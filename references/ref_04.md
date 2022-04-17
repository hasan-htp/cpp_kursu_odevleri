#### Aşağıdaki C++ programı hakkında yorum yapınız:

+ sentaks hatası
+ tanımsız davranış
+ derleyiciye göre değişir
+ ekrana şunu yazar: 

```
#include <iostream>

int main() 
{
	int ival = 1;
	const int &r = ival > 0 ? ival : 1; // sağ taraftaki ifade r value ifadesi. -> &r 'in referansı ival'a değil , geçici bir değişkennin referansıdır.
	ival = 5;
	std::cout << ival << r;
	// 51
}
```

[ödev cevabı](https://vimeo.com/433201294)
