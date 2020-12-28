# DSA-Recursion

// /* 1. Counting Sheep  */
// console.log('1. Counting Sheep:')
// const sheepCountRecursion = function(sheep) {
//   //base case
//   if(sheep === 0) {
//     return `All sheep jumped over the fence`
//   }
//   console.log(sheepCountRecursion(sheep - 1))
//   return `${sheep}: Another sheep jumps over the fence`
// }

// let sheep = 3
// console.log(sheepCountRecursion(sheep))

// /* 2. Power Calculator  */
// console.log(' ')
// console.log('2. Power Calculator:')
// const powerCalculator = function(integer, base) {
//   //base case
//   if( base === 1 ){
//     return integer
//   }
//   //other case
//   if(base <= 0) {
//     return 'exponent should be >= 0'
//   }
//   //General Case
//   return integer * powerCalculator(integer, base -1)
// }

// console.log(powerCalculator(10, 2))
// console.log(powerCalculator(10, 0))


// /* 3. Reverse String */
// console.log(' ')
// console.log('3. Reverse String:')

// const reverseString = function(string) {
//   let splitString = string.split('')
//   let reversedArray = splitString.reverse()
//   let reversedString = reversedArray.toString()
//   let regex = /,/gi
//   let cleanedUpString = reversedString.replace(regex, '')
//   return cleanedUpString
// }

// const reverseStringRecursive = function(string) {
//   //base case
//   //if the string has been reversed return empty string
//   if( string.length === 0) {
//     return ''
//   }
//   //general case
//   //take the last character of the string and return it, remove it from the string
//   //find the length of the string, then remove the last character and also return it
//   return string.slice(-1) + reverseStringRecursive(string.substring(0, string.length - 1))
// }

// let string = 'hello world'
// console.log(reverseStringRecursive(string))

// /* 4. nth Triangular Number */
// console.log(' ')
// console.log('4. nth Triangular Number')

// const nthTrianglarRecursion = function(num) {
//   //base case
//   if (num === 0) {
//   return num + 0
//   }
//   //general case
//   return num + nthTrianglarRecursion(num - 1) 
// }

// console.log(nthTrianglarRecursion(3))

/* 5. String Splitter */
// console.log(' ')
// console.log('5. String Splitter')

// const stringSplitter = function(string) {
//   return string.split('/')

// }

// const stringSplitterRecursion = function(string) {
//   //base case
//   //if there are no more values in the string, return the string
//   //general case
//   //return the first part of the string as a value in an array.  recurse the next value
// return string.slice(0, 5) 
// }
// let string = '02/20/2020'
// console.log(stringSplitterRecursion(string))

// /* 6. Fibonacci */
// console.log(' ')
// console.log('6. Fibonacci')

// let count = 1
// const fibonacci = function(num, ) {
//   //base
// if(num === 0) {
//   return  0
// }
//   //general
//   console.log( num)
//   return count + fibonacci(num - 1, count )
// }

// console.log(fibonacci(7))

// /* 7. Factorial */
// console.log(' ')
// console.log('7. Factorial')

// const factorial = function(num) {
//   //base case
//   if (num == 1) {
//     return num 
//   }
//   //general case
//   console.log(num)
//   return num * factorial(num -1)
// }

// console.log(factorial(5))

/* 8. Find a way out of the maze */
console.log(' ')
console.log(`8. Find a way out of the maze`)
//this is an array or arrays.  you are going through the indecies to see if the value is '', '*' or 'e'.
const findPath = function(maze) {
  //base case
  if (maze == "e") {
    return 'you did it!' 
  }
  //general case
  console.log(maze[0])
  return maze
}


let mySmallMaze = [
    [' ', ' ', ' '],
    [' ', '*', ' '],
    [' ', ' ', 'e']
];

let maze = [
    [' ', ' ', ' ', '*', ' ', ' ', ' '],
    ['*', '*', ' ', '*', ' ', '*', ' '],
    [' ', ' ', ' ', ' ', ' ', ' ', ' '],
    [' ', '*', '*', '*', '*', '*', ' '],
    [' ', ' ', ' ', ' ', ' ', ' ', 'e']
];
console.log(findPath(mySmallMaze))
