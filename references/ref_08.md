#### Sentaks hatası olan satırları belirtiniz:

```

auto a; // init edilmesi lazım
	int &b; // ref init edilmesi lazzm
	auto c = 10;
	int &d = c;
	const auto &e = 20;
	int &f = ++c;
	int &g = c + 5; // bu pr expretion ama lvalue olmalı
	int &&h = c % 2;

	int func(); int &&j = func();
	int &foo(); int &&m = foo(); // foo'nun ret'i int& yani onunla yapılan ilk değer verme lvalue olmaı, &&m r valuıe referans
	int ival = 10; int &&rval = ival + 10; int &p = rval;// valid. // rval data type int&& yani sağ taraf, fakat ifade olarak sol taraf ifadesi, yani sorun yok.


```


[ödev cevabı](https://vimeo.com/433277804)
