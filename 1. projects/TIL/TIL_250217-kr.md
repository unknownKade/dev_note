## Git Actions
Github 월 500mb/2000분 무료
#\.github/workflows 에 yaml로 설정

- Gradle 예시
```yml
# This workflow uses actions that are not certified by GitHub.
# They are provided by a third-party and are governed by
# separate terms of service, privacy policy, and support
# documentation.
# This workflow will build a package using Gradle and then publish it to GitHub packages when a release is created
# For more information see: https://github.com/actions/setup-java/blob/main/docs/advanced-usage.md#Publishing-using-gradle

name: Gradle Package

on:
  release:
    types: [created]

jobs:
  build:
    runs-on: ubuntu-latest
    permissions:
      contents: read
      packages: write

    steps:
    - uses: actions/checkout@v4
    - name: Set up JDK 17
      uses: actions/setup-java@v4
      with:
        java-version: '17'
        distribution: 'temurin'
        server-id: github # Value of the distributionManagement/repository/id field of the pom.xml
        settings-path: ${{ github.workspace }} # location for the settings.xml file

    - name: Setup Gradle
      uses: gradle/actions/setup-gradle@af1da67850ed9a4cedd57bfd976089dd991e2582 # v4.0.0

    - name: Build with Gradle
      run: ./gradlew build

    # The USERNAME and TOKEN need to correspond to the credentials environment variables used in
    # the publishing section of your build.gradle
    - name: Publish to GitHub Packages
      run: ./gradlew publish
      env:
        USERNAME: ${{ github.actor }}
        TOKEN: ${{ secrets.GITHUB_TOKEN }}

```

- CI/CD 파이프라인 예시
```yaml
name: 'CI' #actions 이름

#Event Trigger
#when
on:
	push:
		branches:[dev, feat/*]
	pull_request:
		branches [dev]
#do this
jobs:
	ci: #job name
		runs-on:[ubuntu-latest] #os script is run  on
		steps:
			#job1
			name:checkout
			uses: actions/checkout@v4 #action plugin
			#job2
			name: java setup
			uses: actions/setup-java@v2
			with:
				distribution:'adopt'
				java-version: '17'
			#job3 
			name: run unittest
			run: 
				./gradlew clean test
```