#### Aşağıdaki kodda yapılan referans tanımlamalarından geçersiz olanları işaretleyin ve geçersizlik nedenlerini açıklayın:

```
int &f1();
int f2();

int main()
{
	int x = 10;
	int y = 35;
	const int primes[]{ 2, 3, 5, 7, 11, 13, 17, 19, 23, 29 };
	int a[]{ 1, 2, 4 };
	int &r1; //init edilmesi lazı
	int &r2(++x); 
	int &r3{ 10 }; // l value ile init edilmesi lazım 
	const int &r4{ int() };
	const int &r5{ int{} };
	int &r6 = +y; // must be lvalur
	int &r7 = (x, y);
	int &r8 = x > 10 ? x : y;
	int &r9 = f1();
	int &r10 = f2();// must be lvalur
	int &r11 = primes[5]; // const int olduğu için hata verir
	int const &r12 = *primes; 
	const int &r13{ x };
	int *&r14 = a; // a int* değil
	int(&r15)[] = a; // alttaki gibi olmalı
	int(&r16)[3] = a;
}
```

[ödev cevabı](https://vimeo.com/362516832)
