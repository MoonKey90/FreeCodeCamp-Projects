const units = {
  "PENNY": 1,
  "NICKEL": 5,
  "DIME": 10,
  "QUARTER": 25,
  "ONE": 100,
  "FIVE": 500,
  "TEN": 1000,
  "TWENTY": 2000,
  "ONE HUNDRED": 10000
};

function checkCashRegister(price, cash, cid) {
  
  let cashReturn = Math.round(cash * 100 - price * 100);
  let checkReturn = cashReturn;
  let change = [];
  let status = '';

  let moneyOnCid = 0;
  let filteredCid = cid.filter(elem => elem[1] !== 0).reverse();

  filteredCid.forEach(elem => {
    let money = elem[0];
    let moneySum = elem[1] * 100;
    moneyOnCid += moneySum;
    let amount = 0;
    while (cashReturn >= units[money] && moneySum > 0) {
      amount += units[money];
      cashReturn -= units[money];
      moneySum -= units[money];
    }
    if (amount !== 0) {
      change.push([money, amount / 100]);
    }
  });

  if (cashReturn > 0) {
    status = 'INSUFFICIENT_FUNDS';
    change = [];
  } else if (cashReturn == 0 && checkReturn == moneyOnCid) {
    status = 'CLOSED';
    change = cid;
  } else {
    status = 'OPEN';
  }
  return { 'status': status, 'change': change };

}

checkCashRegister(19.5, 20, [["PENNY", 1.01], ["NICKEL", 2.05],
["DIME", 3.1], ["QUARTER", 4.25], ["ONE", 90], ["FIVE", 55],
["TEN", 20], ["TWENTY", 60], ["ONE HUNDRED", 100]]);