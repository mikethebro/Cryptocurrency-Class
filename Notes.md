## Cryptographic Hash Functions
-mathematical function  
-takes any string as input  
-fixed-size output (Bitcoin uses 256 bits)  
-efficiently computable (computes the output in a reasonable amount of time)  
### Security properties
#### Collision-Free  
-Nobody can find x and y such that x != y and H(x)=H(y)  
-collisions may exist, just ensure nobody can find them  
-collisions WILL exist: with a 256-bit output, there are 2^256 possible outputs  
--there are more than this many **possible** inputs, so there are guaranteed to be collisions  
--however, 2^256 is such a large number that it is almost guaranteed nobody will ever find a collision  
--if every computer ever made was computing since the beginning of time trying to find a collision, still unlikely to find one  
-are there any easy ways to find collisions?  
--with some simple hash functions, there are  
-if we know H(x) == H(y) and we know it's collision-free, we can assume x == y  

#### hiding  
-given H(x), it is infeasible to find x  
-no value of x which is particularly likely (or else it's easy to find x)  
-If r is chosen from a probability distribution that has high min-entropy, then given H(r |x), it is infeasible to find x.  
-High min-entropy means that the distribution is "very spread out", so that no particular value is chosen with more than negligible probability.  
#### puzzle-friendly  
