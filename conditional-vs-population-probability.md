Two different diseases cause a certain weird symptom; anyone who has either or both
of these diseases will experience the symptom. Let D1 be the event of having the first
disease, D2 be the event of having the second disease, and W be the event of having the
weird symptom. Suppose that D1 and D2 are independent with P (Dj ) = pj , and that a
person with neither of these diseases will have the weird symptom with probability w0.
Let qj = 1 − pj , and assume that 0 < pj < 1.
(a) Find P (W ).
(b) Find P (D1|W ), P (D2|W ), and P (D1, D2|W ).
(c) Determine algebraically whether or not D1 and D2 are conditionally independent
given W .
(d) Suppose for this part only that w0 = 0. Give a clear, convincing intuitive explanation
in words of whether D1 and D2 are conditionally independent given W.




Ans -- 
here my personal 1st instinct was to get all the probability of symptoms happening 
so for me P(W) was initially w0 + p1 + p2 - p1p2.
now why did i do that beacuse i thought w0 is the all the people with only the symptom but not disease and -p1p2 is for the ones who are double counted.
After a bit more thinking i found where was my thinking wrong.
It was when i realized that w0 is not in total population it depends on how many people are not infected it's the probability of the people who don't have the disease but have the symptom
not overall population probability.
how did i get it right---------
then i thought about how can i find the probability of not having the symptom
q1 which is prob of not having disease1 and q2 which is prob of not having disease2 and who would not have these are safe and they also don't need to have symptoms so that's 
3 conditions q1 q2 and 1-w0.
so the prob of having the symptom becomes = 1 - (1-w0)q1q2.


now the next prob are compartively easy to find but
the main thing that this question in specififc teaches us is that "independency does not mean conditional independeny".
This problem is another form of Berkson's paradox which means know one thing happened or not directly affects the probability of the second thing happening.
and also another key takeaway from this is that whenever the probability comes we should see "probability on which population".
