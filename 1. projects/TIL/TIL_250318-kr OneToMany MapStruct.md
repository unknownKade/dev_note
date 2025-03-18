``` java

//List객체 매핑하는 경우
@OneToMany(mappedBy = "order", cascade = CascadeType.ALL, orphanRemoval = true)  
private List<OrderProductEntity> orderProducts;

//양방향 매핑
@ManyToOne(fetch = FetchType.LAZY)  
@JoinColumn(name= "orderId")  
private OrderEntity order;

//매핑할 때 양방향으로 넣음
public void setOrder(OrderEntity order){  
  this.order = order;  
}

//Mapper
@Mapper(componentModel = "spring")  
public interface OrderPersistenceMapper {  

//해당 변수에 실행할 매핑 메소드를 qualifiedByName 으로 설정
  @Mapping(target = "orderProducts", qualifiedByName = "toProductEntities")  
  OrderEntity toEntity(Order order);  

//객체 내 리스트도 매핑
  @Named("toProductEntities")  
  List<OrderProductEntity> toProductEntities(List<OrderProduct> orderProduct);  

//Order 안의 Orderproduct 매핑 반대 매핑도 해서 저장 
  @AfterMapping  
  default void setProducts(@MappingTarget OrderEntity order){  
    order.getOrderProducts()  
        .forEach(product -> product.setOrder(order));  
  }  
}

```