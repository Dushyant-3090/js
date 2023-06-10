/* const input = [1, -4, 12, 0, -3, 29, -150];

const value=input.reduce((res,acc)=>{
 acc+=res;
 return acc;
},0)

console.log(value);



const arr = [1, 2, 3, 4, 5];
const result=arr.map((ele)=>{
 return ele*ele;
})
console.log(result);

 */

//3
/* const input = [12, 46, 32, 64];
let sum=0;
const len=input.length;
for(let i=0; i<len; i++){
 sum+=input[i];
}
const mean=sum/len;

let v1=len/2-1;
let v2=len/2;

const med=(input[v1]+input[v2])/2;
console.log(`mean is ${mean} and median is ${med}`); *

 */

//4

/* const input = [
 {
   name: "John",
   age: 13,
 },
 {
   name: "Mark",
   age: 56,
 },
 {
   name: "Rachel",
   age: 45,
 },
 {
   name: "Nate",
   age: 67,
 },
 {
   name: "Jennifer",
   age: 65,
 },
];
let maxi=Number.MIN_SAFE_INTEGER;
let mini=Number.MAX_SAFE_INTEGER;

for(let i=0; i<input.length; i++){
if(input[i].age>maxi){
 maxi=input[i].age;
}
if(input[i].age<mini){
mini=input[i].age;
}

}
const diff=maxi-mini;
console.log(`difference is ${diff}`); */

//5
/* 
function factorial(n) {
  if (n === 0 || n === 1) {
    return 1;
  } else {
    return n * factorial(n - 1);
  }
}

var number = 4;
var result = factorial(number);
console.log(`factorai is ${result}`);


 */
 
 //6
 
 
 const products = [
  { name: "Product 1", price: 20, category: "Electronics" },
  { name: "Product 2", price: 30, category: "Clothes" },
  { name: "Product 3", price: 40, category: "Electronics" },
  { name: "Product 4", price: 50, category: "Clothes" },
  { name: "Product 5", price: 60, category: "Clothes" },
  { name: "Product 6", price: 70, category: "Electronics" },
  { name: "Product 7", price: 80, category: "Clothes" },
  { name: "Product 8", price: 90, category: "Electronics" },
];

const products = [
  { name: "Product 1", price: 20, category: "Electronics" },
  { name: "Product 2", price: 30, category: "Clothes" },
  { name: "Product 3", price: 40, category: "Electronics" },
  { name: "Product 4", price: 50, category: "Clothes" },
  { name: "Product 5", price: 60, category: "Clothes" },
  { name: "Product 6", price: 70, category: "Electronics" },
  { name: "Product 7", price: 80, category: "Clothes" },
  { name: "Product 8", price: 90, category: "Electronics" },
];

function calculateAveragePrice(products, category) {
  const filteredProducts = products.filter((product) => product.category === category);
  const sum = filteredProducts.reduce((total, product) => total + product.price, 0);
  const average = sum / filteredProducts.length;
  return average;
}

function getCategoriesWithAveragePriceAbove50(products) {
  const categories = [...new Set(products.map((product) => product.category))];
  const result = [];

  categories.forEach((category) => {
    const averagePrice = calculateAveragePrice(products, category);
    if (averagePrice > 50) {
      result.push({ category: category, averagePrice: averagePrice });
    }
  });

  return result;
}

const categoriesAbove50 = getCategoriesWithAveragePriceAbove50(products);
console.log(categoriesAbove50);
