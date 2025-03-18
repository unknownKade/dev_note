``` java

//Referenced Table
@OneToMany(mappedBy = "order", cascade = CascadeType.ALL, orphanRemoval = true)  
private List<OrderProductEntity> orderProducts;

//referenced 
@ManyToOne(fetch = FetchType.LAZY)  
@JoinColumn(name= "orderId")  
private OrderEntity order;

@Mapper(componentModel = "spring")  
public interface OrderPersistenceMapper {  
  @Mapping(target = "orderProducts", qualifiedByName = "toProductEntities")  
  OrderEntity toEntity(Order order);  
  
  @Named("toProductEntities")  
  List<OrderProductEntity> toProductEntities(List<OrderProduct> orderProduct);  

  
  @AfterMapping  
  default void setProducts(@MappingTarget OrderEntity order){  
    order.getOrderProducts()  
        .forEach(product -> product.setOrder(order));  
  }  
}

```