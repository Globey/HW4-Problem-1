HW4-Problem-1
=============

<p><b>
Use Sage to investigate the following problem in number theory. *
Let f(x)=x^2 + a*x + b be a quadratic polynomial with integer coefficients, for example, f(x) = x^2+x+6. 
Formulate a conjecture about when the set A={f(n) : n in Z and f(n) is prime} is infinite. 
(NOTE: It is an open problem to prove anything in this direction, so you probably shouldn't try. 
For example x^2+1 is conjectured to be prime infinitely often, but nobody has a proof. Just make a conjecture.) 
</b></p>

<br>
I did this problem in a few stages.

First I created a list of natural numbers up to an arbitrary value(101 in this case) then I applied the given quadratic function, with an arbitrary a and b,
on our list of natural numbers using a list comprehension. I named the list f_of_n.

sage: naturals_list = range(1,101)
sage:a=0
sage:b=1    
sage: f_of_n = [n^2+a*n+b for n in naturals_list]; f_of_n <br>
output:[2, 5, 10, 17, 26, 37, 50, 65, 82, 101, 122, 145, 170, 197, 226, 257,
290, 325, 362, 401, 442, 485, 530, 577, 626, 677, 730, 785, 842, 901,
962, 1025, 1090, 1157, 1226, 1297, 1370, 1445, 1522, 1601, 1682, 1765,
1850, 1937, 2026, 2117, 2210, 2305, 2402, 2501, 2602, 2705, 2810, 2917,
3026, 3137, 3250, 3365, 3482, 3601, 3722, 3845, 3970, 4097, 4226, 4357,
4490, 4625, 4762, 4901, 5042, 5185, 5330, 5477, 5626, 5777, 5930, 6085,
6242, 6401, 6562, 6725, 6890, 7057, 7226, 7397, 7570, 7745, 7922, 8101,
8282, 8465, 8650, 8837, 9026, 9217, 9410, 9605, 9802, 10001]
<br>
Then I took f_of_n and I filtered out everything but the primes so that we were left with a set consisting of primes
and natural numbers. Exactly what we were looking for.


primes_list = []
counter = 0
for p in f_of_n:
    if is_prime(p):
        counter += 1
        primes_list.append(p)

<br>
[2, 5, 17, 37, 101, 197, 257, 401, 577, 677, 1297, 1601, 2917, 3137,
4357, 5477, 7057, 8101, 8837]
<br>
Looking at this list above (what we defined to be set A in the problem in bold), I would just like to note that for here on out I make the 
following assumption that for any set A that I find to contain more than 1 element, I'm going assume that it goes on infinitely, 
even if very slowly. There's no way to know, but I think it's a reasonable assumption and the threshold is going to be
somewhat arbitrary anyways.

<br>

My conjecture:
Let f(x)=x^2 + a*x + b be a quadratic polynomial with integer coefficients. <br>
Also let A = {f(n) : n in Z and f(n)}

I make the conjecture that when both a and b are odd , then the set is infinite.



