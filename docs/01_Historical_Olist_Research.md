# Historical Olist Company Research

## Research Period

The dataset represents orders purchased from 2016 to 2018. The company research should therefore focus on Olist's business model around the same period instead of projecting current capabilities backward.

## Historical Business Model

Based on historical sources from 2017–2018:

- Olist focused on helping small and medium-sized merchants reach consumers through established online marketplaces.
- Olist connected merchants with major marketplace/e-commerce channels rather than requiring each merchant to negotiate separate marketplace relationships.
- The service combined marketplace access with operational support around catalog/product information, orders, payments, delivery, and customer service.
- A 2017 Medium article by Tiago Dalvi describes a hybrid SaaS + Marketplace model with recurring subscription and sales commission components.
- Two 2017 reports describe a 20% commission on sales alongside subscription pricing. This figure is treated as source-reported historical information, not as a metric derived from the dataset.
- Historical sources describe Olist as a large virtual department-store layer made up of small stores and integrated with major marketplaces.

## Ecosystem

```text
Small / Medium Merchants
          |
          v
        Olist
          |
          +---- Major Marketplaces / Retail Channels
          |
          +---- Logistics / Delivery Partners
          |
          v
      Final Consumers
```

## Dataset Mapping

The dataset supports several parts of this historical operating model:

| Historical Business Area | Dataset Evidence |
|---|---|
| Customers | Customers table |
| Orders | Orders table |
| Products | Products table |
| Sellers / Merchants | Sellers table |
| Marketplace transaction items | Order Items table |
| Payments | Payments table |
| Customer feedback | Reviews table |
| Geography | Customer, Seller, Geolocation tables |
| Category structure | Products + Translation tables |
| Delivery lifecycle | Order timestamps |

## Limitations

The dataset does not contain Olist's internal financial statements, subscription revenue, commission revenue, operating costs, or profit. Therefore those business-model elements should be discussed as historical company research, not calculated from the dataset.

## Historical Sources

1. Tiago Dalvi, Medium, 3 May 2017  
https://medium.com/@tiago_dalvi/a-revolu%C3%A7%C3%A3o-na-%C3%A1rea-de-relacionamento-com-o-cliente-no-olist-b9a764da2f68

2. Mercado&Consumo, 26 June 2017  
https://mercadoeconsumo.com.br/26/06/2017/noticias/startup-ajuda-pequenos-lojistas-a-vender-produtos-em-marketplaces/

3. Gazeta do Povo, 14 November 2017  
https://www.gazetadopovo.com.br/economia/nova-economia/olist-quer-ser-a-maior-loja-virtual-dentro-dos-principais-marketplaces-do-pais-3xbe9k4mn13uzs1pm60ym6znz/

4. Pequenas Empresas & Grandes Negócios / Endeavor Brasil, 15 June 2018  
https://revistapegn.globo.com/Banco-de-ideias/E-commerce/noticia/2018/06/tiago-dalvi-da-olist-nenhum-modelo-de-negocio-esta-escrito-em-pedra.html
