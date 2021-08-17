# Construindo um projeto com arquitetura baseada em microsserviços usando Spring Cloud

Este projeto foi desenvolvido como parte as atividades do BootCamp Santander - Fullstack Developer da Digital Innovation One.

O projeto é composto de dois microsserviços PRODUCT-CATALOG e SHOPPING-CART, um servidor de configuração CONFIG-SERVER, um SERVICE-DISCOVERY e um GATEWAY.

Algumas alterações foram necessárias em relação à apresentação original devido aos requisitos de versões mais recentes dos componentes. Entre estas alterações estão:

Application.properties original:
spring.cloud.config.uri=http://localhost:8888

Application properties modificado:
spring.config.import=configserver:http://localhost:8888/

build.gradle original:
set('springCloudVersion', "Hoxton.SR3")

build.gradle modificado: 
set('springCloudVersion', "2020.0.3")

application.properties do Gateway:
spring.main.web-application-type=reactive

## Uso

POST localhost:8080/product - cadastra o produto

GET localhost:8080/product/id - retorna o produto com a id correspondente

POST localhost:8080/cart - cadastra o carrinho

GET localhost:8080/cart/id - retorna o carrinho com a id correspondente