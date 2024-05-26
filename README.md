# SI_2024_lab2_223105
Нина Манасиевска 223105
Група: ПИТ-3

2.Control Flow Graph
![finalv2](https://github.com/ninamanas/SI_2024_lab2_223105/blob/master/CFG.drawio.png)

3.Цикломатска комплексност

Цикломатската комплексност на овој код е 10, истата ја добив преку формулата P+1, каде што P е бројот на предикатни јазли. Во случајoв P=9, па цикломатската комплексност изнесува 10.
Според бројот на региони во Control Flow Graph-от, а бројот на региони на горенаведената слика на графот е 10.

4.Тест случаи според критериумот Every Branch

1 .allItems==nul  => za da go pokrieme prviot exception

2. ( allItems[null,"0123",301,0.1] , 0 )  => so ova kje go pokrieme if-ot za name==null, if-ot za validen barcode, if-ot za discount>0 ,  go pokrivame i sledniov 
  if(item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0') , kako i  if (sum <= payment) koj kje vrati true.
  
3. ( allItems["name",null,200,0.1] , 0 ) => so ovoj test primer kje go pokrieme exceptionot za barcode==null.
   
4. ( allItems["name","12a",200,0.1] , 0 ) => so ovoj test primer go pokrivame frlanjeto na exepcion za nevaliden karakter vo barcode.
   
5. ( allItems["name","123",200,0] , 0 )  => tuka go pokrivame posledniot  if (sum <= payment), odnosno else i kje vrati false.



5. Multiple Condition

if (item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0)== '0')

2^3 => 8 test cases
   
T || X || X -> кога price > 300

F || T || X -> кога price <= 300 но discount > 0

F || F || T -> кога price <= 300, discount <= 0 но barcode почнува на 0 

F || F || F -> кога price <= 300, discount <= 0 и barcodeне започнува на 0

