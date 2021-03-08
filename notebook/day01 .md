Then, what've done today.
I've calculated the chance than real madrid become champion.

this is the program

```javascript
var alphabet = ['V','N','D']
var mots = ['V','N','D']


const generate = function(mots, alphabet) {
  var words = [];
  mots.forEach( mot => 
    alphabet.forEach( alpha =>  
      words.push(mot+alpha)
    )
  )
  return words;
}
/*
const generate0 = (mots) => {
  var words = [];
  mots.forEach( mot => 
    alphabet.forEach( alpha =>  
      words.push(mot+alpha)
    )
  )
  return words;
}

const g = (mots) => {
  w = []
  alphabet.forEach( alpha =>  
    mots.forEach( mot =>
      w.push(mot+alpha)
    )
  )
  return w
}

console.log(g(g(g(g(mots)))))
*/


const reducer = function(acc, val) { 
  if (val === 'V') { 
    return acc+3
  }
  if (val === 'D') { 
    return acc 
  }
  if (val === 'N') { 
    return acc+1 
  }
}

const r0 = Array.from({length: 13},() => 0)
console.log(
  generate(
    generate(
      generate(mots, alphabet)
      , alphabet
    )
  , alphabet)
  .map( x => Array.from(x))
  .map( x => x.reduce(reducer, 0) )
  .forEach(x => r0[x] = r0[x] + 1)
)
const r1 = [...r0]
console.log(r0)
console.log(r1)

const tbl = []
r0.forEach( (n, p) => {
  r1.forEach( (m, q) =>  
    tbl.push([p-q == 0 ? 0 : 1, n*m])
    process.stdout.write("ah ")
})
  process.stdout.write("\r")
   }
)

tbl.reduce((a,x) => 
  [
    a[0]+x[0]*x[1], 
    a[1]+ x[1]
  ], [0,0])

//console.log(tbl.length)
```
