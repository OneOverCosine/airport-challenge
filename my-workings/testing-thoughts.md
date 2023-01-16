# Testing Plans
Here's where I plan my tests.

### **User Story 1**
```
As an air traffic controller   
So I can get passengers to a destination  
I want to instruct the airport to land a plane
```

**Initial Thoughts**  
1. Need an airport
2. Need a plane
3. Need to be able to land the plane
4. Landing a plane is like 'storing' it in the airport - need a plane list, then
5. The plane list should increase by one when a plane is landed


**Test 1 -** when a ``Plane`` is landed, ``planeList`` should increase by 1


### **User Story 2**
```
As the system designer  
So that the software can be used for many different airports  
I would like a default airport capacity that can be overridden as appropriate
```

**Thoughts**  
1. Airport needs a default capacity
2. The capacity needs to be able to be updated

**Test 2 -** when an ``Airport`` is created, it should have a default capacity of 7

**Test 3 -** After an Airport is created, ``updateAirportCapacity`` can be called to change it's capacity


### **User Story 3**
```
As an air traffic controller  
To ensure safety  
I want to prevent landing when the airport is full 
```

**Thoughts**  
1. Need a function to check if the airport is full
2. Need a check before allowing planes to land

**Test 4 -** If ``planeList`` is at max capacity, ``land`` will not add another ``Plane``  


## **User Story 4**
```
As an air traffic controller  
So I can get passengers on the way to their destination  
I want to instruct the airport to let a plane take off and confirm that it is no longer in the airport  
```

**Thoughts**  
1. Need to be able to remove planes from the airport
2. Should be able to remove a specific plane (need the plane id)

**Test 5 -** When ``takeOff`` is called, the length of ``planeList`` should decrease by 1