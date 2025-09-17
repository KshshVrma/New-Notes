pass by reference is much faster then pass by value especially when the passed value increases in size, 

the reason of this is because when the code is converted to assembly code-> 

the system copies the pass by value object bit by bit in a loop, because of this it is extremely slow as compared to pass by reference.