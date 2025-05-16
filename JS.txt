(function() {
    console.log(1); 
    setTimeout(function(){console.log(2)}, 1000); 
    setTimeout(function(){console.log(3)}, 0); 
    console.log(4);
})();

for (let i = 0; i < 5; i++) {
  setTimeout(function() { console.log(i); }, i * 1000 );
}

const module = {
  x: 42,
  y:"A",
  getX: function () {
    return (this.x + this.y);
  },
};

const module2 = {
  x: 22,
  y:"B",
  getX: function () {
    return (this.x + this.y);
  },
};


const unboundGetX = module.getX;
console.log(unboundGetX()); 

const boundGetX = unboundGetX.bind(module2);
console.log(boundGetX()); 


