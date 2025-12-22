# Лабораторная работа 1. Знакомство с IaaS, PaaS, SaaS сервисами в облаке на примере Amazon Web Services (AWS). Создание сервисной модели.

## Цель работы: 
- Получить навыки аналитики и понимания спектра публичных облачных сервисов без привязки к вендору.
- Сформировать комплексное видение Облака.

## Ход работы
### 0. Что такое IaaS, PaaS, SaaS 

IaaS, PaaS, SaaS - классификации, определяющие уровень ответственности между провайдером и клиентом.

* **IaaS (Infrastructure as a Service)**
Провайдер предоставляет абстрактную вычислительную инфраструктуру: виртуальные процессоры, память, диски, сети.
Клиент может управлять почти всем: операционными системами, средами выполнения, приложениями, данными, конфигурациями безопасности.

* **PaaS (Platform as a Service)**
Провайдер предоставляет готовую платформу: ОС, инструменты, базы данных, веб-серверы.
Клиент контролирует разрабатываемый код приложения и данные.

* **SaaS (Software as a Service)**
Провайдер предоставляет полностью готовое к использованию программное обеспечение доступное через сеть.
Клиент контролирует только собственные данные и настройки внутри предоставленного приложения.

### 1. Заполнение таблички

**Чтобы заполнить данную мне табличку (team 7), я делал несколько шагов:** 
1) Смотрим на данные нам в варианте поля: Product Code,	Usage Type,	lineItem/Operation,	lineItem/LineItemDescription
2) Определяем по порядку ```IT Tower -> Service Family -> Service Type -> Service Sub Type	-> Service Usage Type```.
3) Service Family легко узнать на официальном сайте AWS просто вбив Product Code:
<img width="1588" height="540" alt="image" src="https://github.com/user-attachments/assets/98dd6465-6f7b-4a1f-9d76-9fb643183d3f" />

4) По данной в примере табличке определяем IT Tower: 
<img width="303" height="392" alt="image" src="https://github.com/user-attachments/assets/c6c288b2-16b2-4cc2-b73f-149027287729" />

5) Service Type — это просто понятное название конкретного продукта AWS.
```
AmazonS3 → Service Type: Amazon S3
AmazonMSK → Service Type: Amazon MSK (Managed Streaming for Kafka)
AmazonES → Service Type: Amazon OpenSearch
AmazonMacie → Service Type: Amazon Macie
AmazonPolly → Service Type: Amazon Polly
AmazonPersonalize → Service Type: Amazon Personalize
```
6) Service Sub Type	и Service Usage Type определяем по Usage Type,	lineItem/Operation,	lineItem/LineItemDescription:
* Service Sub Type - буквально подтип сервиса.
Чтобы понять его (и простить) ищем в Usage Type индекаторы (все что идет после % - региона), и далее ищем по ним в интернете. Я использвал сайты:
- https://aws-docsearch.netlify.app/docs/aws-usage-report-understand/
- https://aws.amazon.com
- ну и гугл с нейронками, если все плохо
  
* Service Usage Type - означает в каких единицах это измеряется или какая конкретно операция была выполнена:
Для определения также используем данные нам Usage Type,	lineItem/Operation,	lineItem/LineItemDescription, ну и service sub type:
- на самом деле, как я понял, он обычно и написан как индекатор в Usage Type
- если он непонятен, то ищем в интернете

*Все что имеет ```lineItem/LineItemDescription - Tax%```:*
```
Service Sub Type - Additional Costs
Service Usage Type - Tax
```
*Все что имеет ```lineItem/Operation - RunBroker```:*
```
Service Sub Type - RunBroker
Service Usage Type - RunBroker
```
### 2. Итог
<img width="1382" height="588" alt="image" src="https://github.com/user-attachments/assets/e1b77d56-39e9-4a48-8024-62fc9b5215e3" />
<img width="1374" height="436" alt="image" src="https://github.com/user-attachments/assets/d8a62278-27c4-4804-9ac5-5aa5086987f1" />


