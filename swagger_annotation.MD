## 概念阐述

Swagger提供了一套注解用于描述接口契约，用户使用注解，可以在代码中增加对于契约的描述信息。ServiceComb支持其中的部分注解。

## 场景描述

通过使用注解描述接口契约，用户可以利用ServiceComb的Swagger契约生成功能自动生成符合要求的契约文件，而不用手工编写契约，能够有效提高开发效率。

## 配置说明

关于Swagger注解的含义，可以在[Swagger注解文档](https://github.com/swagger-api/swagger-core/wiki/Annotations-1.5.X)中找到官方说明。您可以对照该官方文档与本说明来了解如何在ServiceComb框架下使用注解指定Swagger契约的各项属性。

### `@Api`

> `@Api`作用于类级别，在Swagger官方描述中是用于将一个Class标注为一个Swagger资源。但该注解在ServiceComb中不是必须的，ServiceComb可以根据`@RestSchema`和`@RpcSchema`确定需要从哪些类中解析出Swagger契约。<br/>
ServiceComb当前支持的属性只有tags。

- tags<br/>
设置当前Class下定义的operation的默认tag值。

### `@SwaggerDefinition`

> `@SwaggerDefinition`作用于类级别，用于定义一个Swagger资源中的信息。

- info
  + description<br/>

  + version

## 示例代码
