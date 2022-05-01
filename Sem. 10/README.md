## Шаблони
Функция/клас, която работи не с променливи от някакъв дефиниран тип, а с абстрактни променливи, се нарича шаблонна функция/клас
```c++
#include <iostream>
using namespace std;

template <class T>
T sum(T a, T b)
{
    return a + b;
}

int main()
{
    int a = 4;
    int b = 9;
    cout << sum<int>(a, b) << endl;

    double c = 3.14;
    double d = 4.5;
    cout << sum<double>(c,d) << endl;
	
    return 0;
}
```
Компилаторът генерира т. нар. шаблонна функция, като замества параметрите на шаблона с типовете на съответните фактически параметри.

**Задача:**
Релизирайте структурата от данни стек(Stack).
![enter image description here](https://www.softwaretestinghelp.com/wp-content/qa/uploads/2019/06/pictorial-representation-of-stack.png)

**Пример**:
 ```c++
int main()
{
   Stack st;


   for(int i = 0; i <  1000; i++)	{
		st.push(i);
	}

	Stack st1 = st;
	Stack st2;
	st2 = st1;

	while (!st2.empty())
	{
		cout << st2.pop() << ' ';
	}
	cout << endl;

   return 0;
}
 ```
