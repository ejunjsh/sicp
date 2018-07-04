

     (define (square x) (* x x)) 
  
    (define (sumsquares x y) (+ (square x) (square y))) 
    
    (define (sqsumlargest a b c) 
        (cond  
            ((and (>= a c) (>= b c)) (sumsquares a b)) 
            ((and (>= b a) (>= c a)) (sumsquares b c)) 
            ((and (>= a b) (>= c b)) (sumsquares a c)))) 



    (sqsumlargest 1 2 3) 
    ;Value: 13 
    (sqsumlargest 1 1 1) 
    ;Value: 2 
    (sqsumlargest 1 2 2) 
    ;Value: 8 
    (sqsumlargest 1 1 2) 
    ;Value: 5 