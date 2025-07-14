和自定义类实现枚举差不多，但是内部创建对象只需要写SUMMER(String name,String description)//写在最前面，并且不是class是enum

**示例**

```
enum SeasonEnum{
    SUMMER("Summer", "The hottest season"),
    WINTER("Winter", "The coldest season"),
    SPRING("Spring", "The time of flowers and fruits"),
    FALL("Fall", "The time of leaves and frost");
    private String name;
    private String description;
    SeasonEnum(String name, String description){
        this.name = name;
        this.description = description;
    }
    public String getName(){
        return name;
    }
    public String getDescription(){
        return description;
    }
}
```

