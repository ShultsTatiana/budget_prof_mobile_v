# budget_prof_mobile_v
Programming assignment: Personal budget, professional mobile version. 5 week, brown belt

Реализуйте систему ведения личного бюджета. <br/> 
# Необходимо обрабатывать запросы следующих типов: <br/>
- `ComputeIncome` _from to_: вычислить чистую прибыль за данный диапазон дат. <br/>
- `Earn` _from to_ **value**: учесть, что за указанный период (равномерно по дням) была заработана сумма value. <br/>
- `PayTax` _from to_ **percentage**: заплатить налог percentage в каждый день указанного диапазона. Это означает простое умножение всей прибыли в диапазоне на (1 - percentage/100), независимо от того, отдавался ли уже налог за какой-то из указанных дней. Прибыль за эти дни, которая обнаружится позже, налогами из прошлого не облагается. <br/>
- `Spend` _from to_ **value**: потратить указанную сумму равномерно за указанный диапазон дат. Чистая прибыль в запросах ComputeIncome вычисляется как разница заработанного (за вычетом налогов) и потраченного. При расчёте налога потраченные суммы не учитываются. <br/>

## Примечания: <br/>
Во всех диапазонах _from to_ обе даты _from_ и _to_ включаются. <br/>

## Формат ввода  <br/>
- В первой строке вводится количество запросов `Q`, затем в описанном выше формате вводятся сами запросы, по одному на строке. <br/>
- Все даты вводятся в формате `YYYY-MM-DD`. Даты корректны (с учётом високосных годов) и принадлежат интервалу с 2000 до 2099 гг. <br/>
- **value** — положительные целые числа, не превышающие 1000000. <br/>
- Гарантируется, что **percentage** — целое число от 0 до 100. <br/>

## Формат вывода  <br/>
- Для каждого запроса `ComputeIncome` в отдельной строке выведите вещественное число — чистую прибыль (прибыль за вычетом налогов) за указанный диапазон дат. <br/>
- Используйте std::сout.precision(25)  в вашем коде для единообразия формата вывода вещественных чисел <br/>

## Ограничения
- Количество запросов Q — натуральное число, не превышающее 100'000. <br/>
- 2.5 секунды на обработку всех запросов.  <br/>
