NO.1 Ajax

ajax1(x(), function(data1){
    ajax2(y(data1), function(data2){
        ajax3(z(data2), function(data3){
              .......
        })
    })
})


NO.2 Promise

var request1 = function(){
    return new Promise(function(resolve, reject){
          ajax1(x(), function(data){
              resolve(data)
          })
    })
}

var request2 = function(param){
    return new Promise(function(resolve, reject){
          ajax2(x(param), function(data){
              resolve(data)
          })
    })
}

var request3 = function(param){
    return new Promise(function(resolve, reject){
          ajax3(x(param), function(data){
              resolve(data)
          })
    })
}

request1()
    .then(function(data1){
        request2(data1);
    }).catch()
    .then(function(data2){
        request3(data2);
    }).catch()
    .then(function(data3){
        ......
    }).catch()
  

NO.3  Async, Await

async function request(){
  var data1 = await request1().catch()
  var data2 = await request2(data1).catch()
  var data3 = await request3(data2).catch()
  ......
}
