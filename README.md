HW4-Problem-1
=============

<p><b>
Use Sage to investigate the following problem in number theory. *
Let f(x)=x^2 + a*x + b be a quadratic polynomial with integer coefficients, for example, f(x) = x^2+x+6. 
Formulate a conjecture about when the set {f(n) : n in Z and f(n) is prime} is infinite. 
(NOTE: It is an open problem to prove anything in this direction, so you probably shouldn't try. 
For example x^2+1 is conjectured to be prime infinitely often, but nobody has a proof. Just make a conjecture.) 
</b></p>

<br>

naturals_list = range(1,101)
a=0
b=1    
f_of_n = [n^2+a*n+b for n in naturals_list]

<br>




My conjecture:
Let f(x)=x^2 + a*x + b be a quadratic polynomial with integer coefficients. <br>
Also let A = {f(n) : n in Z and f(n)}

I make the conjecture that when both a and b are odd , then the set is infinite.



