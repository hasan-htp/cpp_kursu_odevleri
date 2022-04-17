#### Aşağıdaki C++ programı hakkında yorum yapınız:

+ sentaks hatası
+ tanımsız davranış
+ derleyiciye göre değişir
+ ekrana şunu yazar: 

```
#include <iostream>

int foo(int &x, int &y) 
{
	x = 3; // main'deki x = 3
	y = 4; // maindeki x = 4
	return x + y; //ret = 8
}

int main() 
{
	int x = 1;
	int y = 2;
	int z = foo(x, x);

	std::cout << x << y << z;
	//428
}

```

[ödev cevabı](https://vimeo.com/433211545)
