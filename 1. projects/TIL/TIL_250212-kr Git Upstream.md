## Git Upstream Downstream
- 저장소의 흐름을 바탕으로 상대적으로 main에 상대적으로 가까운 위치를 가리키는 개념
- upstream : origin
- downstream : origin에서 멀어지는 방향 예시로 local

``` bash
%% pull main branch %%
git pull origin
%% make dev branch locally %%
git branch --create dev
git switch dev
%% push to a new dev branch %%
git push --set-upstream origin dev
%% merge local dev code to main branch %%
git switch main
git merge dev
git push origin
%% compare remote with local %%
git fetch
git status

%% from fork add upstream original remote %%
git clone <fork url>
git remote add upstream <url of origin you forked from>

```

## 참고
[How to Add Upstream in Git](https://www.geeksforgeeks.org/how-to-add-upstream-in-git/)