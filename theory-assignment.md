
# `Learn React With Harshi` Series 
   Documenting my learning journey of [Namaste React Live Course](https://learn.namastedev.com/) conducted by Akshay Saini

## Theory Assignment: `Chapter - 06 Exploring the world` (14/01/2023)

###  1. What is a Microservice?
  Microservice Architecture is an architectural style that structures the application as a collection of services which are independently deployable, based on Separation of Concern (SoC),  loosely coupled, owned by small teams, highly maintainable and testable , communicating through lightweight protocols (APIs). The microservice architecture enables the rapid, frequent and reliable delivery of large, complex applications. It also enables an organization to evolve its technology stack.

  Microservices are an architectural and organizational approach to software development where software is composed of small independent services that communicate over well-defined APIs. These services are owned by small, self-contained teams.

Examples : Netflix became one of the first high-profile companies to successfully migrate from a monolith to a cloud-based microservices architecture in 2009. 

### 2. What is  Monolith architecture?
  Monolith Architecture is the traditional model of software development where the application is self-contained and independent of other applications. It is also called Single Tier (One tier) architecture where a single application acts as both client and server. A small change in a single function requires compiling and testing the entire application, which is against the today's agile approach.
### 3. What is the difference between Monolith and Microservice?
 | Parameters   | Monolith Architecture  | Microservices Architecture  |
 | ------------ | --------------------   | :-------------------------: |
 | Development | When an application is built with one code base, it is easier to develop. This is true for small applications, but when the application takes larger, development becomes slower and complex    | Micro services add more complexity compared to monolith arch. If development sprawl isn’t properly managed, it results in slower development speed and poor operational performance.   |
 | Testing | Since a monolithic application is a single, centralized unit, end-to-end testing can be performed faster than with a distributed application. | Teams can experiment with new features and roll back if something doesn’t work. This makes it easier to update code and accelerates time-to-market for new features. Plus, it is easy to isolate and fix faults and bugs in individual services. |
 | Performance | In a centralized code base and repository, one API can often perform the same function that numerous APIs perform with microservices | Though performance could be an issue in microservices, it could be over come by various performance optimisation techniques | 
 | Debugging  | With all code located in one place, it’s easier to follow a request and find an issue. |  Each microservice has its own set of logs, which makes debugging more complicated. Plus, a single business process can run across multiple machines, further complicating debugging. |
 | Scalability | You can’t scale individual components |If a microservice reaches its load capacity, new instances of that service can rapidly be deployed to the accompanying cluster to help relieve pressure.|
 | Relaibility | If there’s an error in any module, it could affect the entire application’s availability. | You can deploy changes for a specific service, without the threat of bringing down the entire application.|
 | Tech Adoption | Any changes in the framework or language affects the entire application, making changes often expensive and time-consuming. | Any new tech changes can eaily be adopted as an independent service | 
 | Deployment |    One executable file or directory makes deployment easier. But, a small change to a monolithic application requires the redeployment of the entire monolith.      |  Microservices make it easier for teams to update code and accelerate release cycles with continuous integration and continuous delivery (CI/CD).   |
 | Agility | There is no agility in monolith | Promote agile ways of working with small teams that deploy frequently. |
### 4. Why do we need a useEffect Hook?
  `useEffect` Hook is used to synchronize a component with the external system. 

  ```
  useEffect(setup, dependencies?)
  ```
  where :
  `setup` - is a function wuth the Effect's logic. 
   
  `dependencies` - List of values that the setup function will depend on. 



### 5. What is Optional Chaining?

The optional chaining `(?.)` operator accesses an object's property or calls a function. If the object accessed or function called is `undefined or null`, it returns `undefined` instead of throwing an error.

The `?.` operator is like the `. chaining operator`, except that instead of causing an error if a reference is nullish (null or undefined), the expression short-circuits with a return value of `undefined`. When used with function calls, it returns `undefined` if the given function does not exist.

*Uses of Optional chaining* : 
1. Exploring the content (nested properties) of an object before accessing its deeply nested sub-porperties. 
2. By using the ?. operator instead of just ., JavaScript knows to implicitly check to be sure obj?.prop is not null or undefined before attempting to access its sub-porperties obj?.prop?.subprop
3. Optional chaining cannot be used on a non-declared root object, but can be used with a root object with value undefined.
Eg : const obj = undefined ; ---> This is possible 
But undeclaredVar?.prop; ---> This throws ref error

### 6. What is Shimmer UI?
From a user experience (UX) perspective, the most important thing is to show your users that loading is taking place. One popular approach to communicate to users that data is loading is to display a chrome color with a shimmer animation over the shapes that approximate the type of content that is loading. Earlier, page loaders were used where a loading progress bar might be displayed before the page is rendered. But, that approach was not that UX friendly. So, Shimmer was introduced.

Shimmer can be skeleton to the actual layout that will be displayed before the data fetch. This will make the user understand what type of layout is loading.
### 7. What is the difference between JS expression and JS statement

`JS Expression` - A js expression produces a value. A number, string,ternary conditions (return true or false), math opertions and array map method (returns new array) are all examples of js expression. 

```
1. "Harshi" -> String is a valid expression 

2. 1234    -> Number is a valid expression 

3. (isLoggedIn) ? "Logout" : "Login"    -> Ternary operator returning value is a valid expression

4. [1,2,3,4].map(num => num*2)  -> array map function is a valid expression which returns a new array after transformation

5. (1+2+3)   -> math operation is a valid expression

```

`JS Statement` - A js statement just executes/performs an action but does not return/produce a value. A variable assignment, if condition (with no return) and for loops are examples of js statement. 

```
1. console.log("This is a js statement")  -> This does not return any value, just prints the content on screen.

2. let name = "Harshi";  -> Variable assigment is a statement 

3. if(true){
    console.log("true"); 
  } else {
    console.log("true"); 
  }   -> This does not return any value

4. for(let i=0; i< 5; i++) {
    arr.push(i);
  } 

```

Having said that, we can't put any js code inside {} in jsx of React. Only `js expressions` can be enclosed within {} of jsx. 


### 8. What is Conditional Rendering, explain with a code example
Your components will often need to display different things depending on different conditions. In React, you can `conditionally render` JSX using JavaScript syntax like `if statements`, `&&`, and `? :` operators.

- `if statements`

- `&&` operator 

- `? :` operator
### 9. What is CORS?

### 10. What is async and await? 

### 11. What is the use of `const json = await data.json();` in  getRestaurants()
