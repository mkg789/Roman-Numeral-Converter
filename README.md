# Roman Numeral Converter
Convert the given number into a roman numeral.




![Roman Numal Converter](https://github.com/mkg789/Roman-Numeral-Converter/assets/126147162/065b2d36-3e90-43d6-b873-1ea8a679ae12)





All roman numerals answers should be provided in upper-case.
'''function convertToRoman(num) {
  const obj ={
    "M":1000,
    "CM":900,
    "D":500,
    "CD":400,
    "C":100,
    "XC":90,
    "L":50,
    "XL":40,
    "X":10,
    "IX":9,
    "V":5,
    "IV":4,
    "I":1
  }
  let roman = "";
  let sum = 0;
  const keys = Object.keys(obj);
  for(const key of keys){
    while(sum+obj[key]<=num){
      sum+=obj[key];
      roman+=key;
    }
  }
  
 return roman;
}

convertToRoman(36);
console.log(convertToRoman(2));
'''
