---
layout: post
title:  "소스코드를 업데이트 방법을 테스트중입니다."
---
```
// header

template <typename T>
class eQueue
{
protected:
	_node<T>* Head;
	_node<T>* Tail;
	_node<T>* temp;

public:
	int Length = 0;

	void Enque(T t);
	T Deque();
};
```

```
//cpp

template <typename T>
void eQueue<T>::Enque(T t)
{
	_node<T>* newNode = new _node<T>(t);

	if (Head == nullptr)
	{
		Head = newNode;
	}
	else
	{
		Tail = Head;
		while (Tail != nullptr)
		{
			temp = Tail;
			Tail = Tail->next;
		}
		Tail = newNode;
		temp->next = Tail;
	}
	Length++;
}

```

```
// cpp

template <typename T>
void eQueue<T>::Enque(T t)
{
	_node<T>* newNode = new _node<T>(t);

	if (Head == nullptr)
	{
		Head = newNode;
	}
	else
	{
		Tail = Head;
		while (Tail != nullptr)
		{
			temp = Tail;
			Tail = Tail->next;
		}
		Tail = newNode;
		temp->next = Tail;
	}
	Length++;
}

```
