Function.prototype.mybind = function (context) {
  let fn = this;
  return function () {
      fn.call(context)
  }
};
// Generic .bind polyfil




Function.prototype.mybind = function (context, ...args1) {
  let fn = this;
  return function (...arg2) {
      fn.apply(context, [...args1, ...arg2])
  }
};

// .bind polyfill with spread operator
