function convertToRoman(num) {
  const dictionary = {
    '1' : "I",
    '4' : "IV",
    '5' : "V",
    '9' : "IX",
    '10' : "X",
    '40' : "XL",
    '50' : "L",
    '90' : "XC",
    '100' : "C",
    '400' : "CD",
    '500' : "D",
    '900' : "CM",
    '1000' : "M",
    '5000' : "Û"
  }

  function find(num) {
  const keys = Object.keys(dictionary)

    for(let i = keys.length -1 ; i >= 0; i--) {
      if( num >= keys[i] && num < keys[i + 1]) {
        return { key: parseInt(keys[i]), symbol: dictionary[keys[i]]}
      }
    }
    return { symbol: "", key: 0 }

  }

    if( num <= 0 ){
      return "" } else {
      const { symbol, key } = find( num )
      return symbol + convertToRoman (num - key)
    }

}

convertToRoman(36);