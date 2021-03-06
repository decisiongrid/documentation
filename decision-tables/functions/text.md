# Text

## **TEXT** functions

* CONCAT
* CONCAT\_WS
* LEN
* REPLACE
* UPPER\_CASE
* LOWER\_CASE

### Concatenation function \(CONCAT\)

The CONCAT function adds two or more strings together.

* Minimum 2 parameters.
* Any quantity of parameters.
* CONCAT can be a part of an embedded function.
* Must be a string, number, or an **INPUT** variable.
* Parameters can be separated by **comma** \(,\).

{% hint style="warning" %}
The separator between the words is a **space**.
{% endhint %}

#### CONCAT function examples:

```javascript
INPUT = "Bye"
[function] --> [output]

CONCAT("Hello", "World")              --> "Hello World"
CONCAT("Hello", "World", "Here")      --> "Hello World Here"
CONCAT(1, 2)                          --> 1 2
CONCAT({INPUT}, "hi")                 --> "Bye hi"
CONCAT(Hello)                         --> invalid
CONCAT(ha, he)                        --> invalid
```

### Concatenation with a separator function \(CONCAT\_WS\)

The CONCAT\_WS function adds two or more strings together with a separator.

* Minimum 2 parameters and the separator.
* Any quantity of parameters.
* CONCAT\_WS can be a part of an embedded function.
* Must be a string, number, or an **INPUT** variable.
* Parameters can be separated by **comma** \(,\).

{% hint style="warning" %}
The separator between the words is what is in the first place in the function CONCAT\_WS\(-, xx, yy\). **-** is the separator **xx-yy**
{% endhint %}

#### CONCAT\_WS function examples:

```javascript
INPUT = "Bye"
[function] --> [output]

CONCAT_WS("-", "Hello", "World")            --> "Hello-World"
CONCAT_WS("+", "Hello", "World", "Here")    --> "Hello+World+Here"
CONCAT_WS("k", "1", "2")                    --> "1k2"
CONCAT_WS("-", {INPUT}, "hi")               --> "Bye-hi"
CONCAT_WS(-, Hello)                         --> invalid
CONCAT_WS(-, ha, he)                        --> invalid
```

### Length function \(LEN\)

The LENfunction returns the length of a string.

* Must have 1 parameter.
* LEN can be a part of an embedded function.
* Must be a string, number, or an **INPUT** variable.

#### LEN function examples:

```javascript
INPUT = "Bye"
[function] --> [output]

LEN("Hello")       --> 5
LEN("555")         --> 3
LEN("Hello")       --> 7
LEN({INPUT})       --> 3
LEN(Hello, bye)    --> invalid
LEN(25)            --> invalid
```

### Replace function \(REPLACE\)

The REPLACE function replaces all occurrences of a substring within a string with a new substring.

* Must have 3 parameters.

{% hint style="warning" %}
1. parameter --&gt; **where** to replace
2. parameter --&gt; **what** to replace
3. parameter --&gt; **for what** to replace
{% endhint %}

* REPLACE can be a part of an embedded function.
* Must be a string, number, or an **INPUT** variable.
* Parameters can be separated by **comma** \(,\).

#### REPLACE function examples:

```javascript
INPUT = "Bye bye"
[function] --> [output]

REPLACE("Hello World", "o", "a")       --> "Hella warld"
REPLACE("Hello 777", "777", "444")     --> "Hella 444"
REPLACE({INPUT}, "y", "3")             -->" B3e B3e"
REPLACE(Hello World, ddd o, a)         --> invalid
REPLACE("Hello World", o, a)           --> invalid
```

### Upper case function \(UPPER\_CASE\)

The UPPER\_CASE function converts the string to the upper case.

* Must have 1 parameter.
* UPPER\_CASE can be a part of an embedded function.
* Must be a string or an **INPUT** variable.

#### UPPER\_CASE function examples:

```javascript
INPUT = "Bye"
[function] --> [output]

UPPER_CASE("Hello World")       --> "HELLO WORLD"
UPPER_CASE("I AM NEW HERE")     --> "I AM NEW HERE"
UPPER_CASE("2ae3")              --> "2AE3"
UPPER_CASE({INPUT})             --> "BYE"
UPPER_CASE("Hello", "no")       --> invalid
UPPER_CASE(Hello World)         --> invalid
```

### Lower case function \(LOWER\_CASE\)

The LOWER\_CASE function converts the string to the upper case.

* Must have 1 parameter.
* LOWER\_CASE can be a part of an embedded function.
* Must be a string or an **INPUT** variable.

#### LOWER\_CASE function examples:

```javascript
INPUT = "Bye"
[function] --> [output]

LOWER_CASE("HELLo WORLd")       --> "hello world"
LOWER_CASE("I am HERE")         --> "i am here"
LOWER_CASE("2AE3")              --> "2ae3"
UPPER_CASE({INPUT})             --> "bye"
LOWER_CASE(Hello, no)           --> invalid
LOWER_CASE(Hello World)         --> invalid
```

