# Assignment3.2
Obtain the elements of the union between two character vectors. ans:
vec1 = c(rownames(mtcars[1:15,]))

vec2 = c(rownames(mtcars[10:32,]))

vec12<-union(vec1, vec2) # returns all the elements of vec1 and vec2 without repeating common elements

vec12

Get those elements that are common to both vectors. ans:
vec1 = c(rownames(mtcars[1:15,]))

vec2 = c(rownames(mtcars[10:32,]))

commonvec12<-vec1%in%vec2 # gives position of common elements

vec1[commonvec12] # gives elements

intersect(vec1,vec2)# alternate way to get intersection of 2 sets of data

Get the difference of the elements between two character vectors. ans:
vec1 = c(rownames(mtcars[1:15,]))

vec2 = c(rownames(mtcars[10:32,]))

vec1[!vec1%in%vec2]# elements of vec1 which are not present in vec2

vec2[!vec2%in%vec1]# elements of vec2 which are not present in vec1

union(vec1[!vec1%in%vec2],vec2[!vec2%in%vec1])#elements which are not common in vec1 and vec2

#alternate way

setdiff(vec1, vec2)# elements of vec1 which are not present in vec2

setdiff(vec2,vec1)# elements of vec2 which are not present in vec1

Test the quality of two character vectors. ans:
vec1 = c(rownames(mtcars[1:15,]))

vec2 = c(rownames(mtcars[11:25,]))

is.element(vec1,vec2)

identical(vec1,vec2)

setequal(vec1,vec2)

vec1 %in% vec2
