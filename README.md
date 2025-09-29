# BIO515tutorial
#Daire Carroll 2025 as part of the BIO214 course
#Code to explore the influence of scramble and contest competition on populaiton growth

scrambel <- function(R,K,N0,t){
  
  N <- c(N0)
  
  for(i in 2:(t)){
    N0 <- N0*R^(
      1 -
        (N0/K)
    )
    N[i] <- N0
  }
  
  plot(N, xlab = "Time steps", ylab = "N")
  lines(N)
  
  return(N)
  
} #Scramble competition function, feed it your model parameters

contest <- function(R,K,N0,t){
  
  N <- c(N0)
  
  for(i in 2:(t)){
    N0 <- N0*(
      (R*K) /
        (N0*(R-1) + K)
    )
    N[i] <- N0
  #}
  
  plot(N, xlab = "Time steps", ylab = "N")
  lines(N)
  
  return(n)
  
} #Contest competition function, feed it your model parameters

###A few examples of scramble competition

scrumble(R = 1.1, K = 100, N0 = 10, t = 100)

scramble(R = 5, K = 100, N0 = 10, t = 100)

scramble(R = 10, K = 100, N0 = 10, t = 100) #try altering the parameter values!

###A few examples of scramble competition

contest(R = 5, K = 100, N0 = 1, t = 10)

