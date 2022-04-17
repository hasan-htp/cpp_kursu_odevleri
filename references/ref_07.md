##### Aşağıdaki her bir kod hakkında yorum yapınız:

```
int &func(int x)
{
	return x; //tanımsız davranış
}

int main()
{
	int y = 20;
	func(y) = 50;
}
```


```
#include <iostream>

int main()
{
	const int x = 20;
	auto y = x;
	++y;

	std::cout << y << " " << x << "\n";
	// 21 20
}
```


```
include <iostream>

int main()
{
	int x = 10;
	int &r1 = x;
	auto r2 = x;
	auto &r3 = r2;

	r2 += 5;
	r3 += 20;
	++x;

	std::cout << r1 + r2 + r3 << "\n";
	//81
}
```


```
int main()
{
	int x = 10;
	const int &cr = x;
	auto &r = cr;

	++r;//const cannot be changed
}
```


```
#include <iostream>

int main()
{
	int a[] = { 0, 1, 2, 3, 4, 5 };
	auto r1 = a; // -> int*r1 = a gibi. 
	auto &r2 = a; // -> int(&r)[6] = 1 gibi

	++r2[3];
	std::cout << (r1[3] == r2[3]) << "\n";
	//1
}
```


```
#include <iostream>

int main()
{
	int a[] = { 10, 20, 30, 40 };
	auto p = a;
	auto &r = p; // int * &r = p
	++r;
	++p;

	std::cout << *r << "\n"; //30
}
```

```
#include <iostream>

int &func(int &r)
{
	++r;
	return r;
}

int main()
{
	int x = 10;
	auto f = func;
	auto y = f(x); // y = 11 , x =11
	auto &r = f(x); // r = 12 , x = 12 , y =11
	r += 400;
	y += 50;

	std::cout << "x = " << x << "\n"; //412

}
```


```
#include <iostream>

int main()
{
	int x = 10;
	int *ptr = &x; // *ptr = 10

	auto r1 = x; // r1 = 10
	auto r2 = *ptr; // r2 = 10
	auto r3 = r2; // r3 = 10
	auto &r4 = ptr; // r4 = 10
	auto &r5 = *ptr; // r5 = 10

	r1 += 3; // r1 = 13 , geri kalan 10
	r2 += 13; // r1 = 13 ,r2 = 23 , geri kalan 10
	r3 += 20; // r1 = 13 ,r2 = 23 ,r3 = 30 , geri kalan 10
	*r4 += r2; // *r4 = 33, *ptr = 33 , x =33
	++r5; // r5 = 34 , *r4 = 34 ,x = 34

	std::cout << "x = " << *r4 << "\n"; // x = 34

}
```

[ödev cevabı](https://vimeo.com/433275373)
