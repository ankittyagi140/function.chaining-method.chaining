# function.chaining-method.chaining
//this is how closures work in Javascript

function mathodsLibrary() {
  let sum = 0;
  const obj = {
    add(...args) {
      sum = [...args].reduce((acc, val) => acc + val, sum);
      return obj;
    },
    subtract(...args) {
      sum = [...args].reduce((acc, val) => acc - val, sum);
      return obj;
    },
    multiply(multiplier) {
      sum = sum * multiplier;
      return obj;
    },
    divide(divisor) {
      sum = sum / divisor;
      return obj;
    },
    result() {
      return sum;
    }
  };
  return obj;
}
const methods = mathodsLibrary();
const output = methods.add(5, 5).multiply(10).result();
console.log(output);
