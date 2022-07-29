# TypeScript で学ぶ テスト駆動開発と async/await

Pythonista のみなさん。型付言語も学んでみませんか？Python に対する見え方も変わってきますよ

# JavaScript の利点

- 環境構築は不要！(ブラウザで動く)
- Web上に簡単に公開できる！

# **JavaScriptさくっと入門**

C言語風の書き方のPythonだと思えば大丈夫

（JavaScript は Python と同じ動的型付け言語なので、型を明示的に書かない）

(実は末尾のセミコロンは省略可能で、小田川はよく省略している)


```javascript
// はコメント
let x = 10; // int x = 10;
var x2 = 10; // 古い書き方
const world = "World"; // 定数．再代入不可。let よりできるだけ const を使うべき

if (x === 10) { // 10 == "10" -> true (ファジーな比較が==なので===を使うべき)
    x++;
}
while (x >= 9 && x !== 20) x--;
for (let i = 0; i < 10; i++) {
    console.log("Hello " + world); // => Hello World がプリントされる
		console.log(`Hello ${world}`); // => Hello World (上よりおすすめ)
    console.log(i);
    console.log(`i: ${i}`); // => i: 0
    
    // break, continueもCと同様
}

function addOne(x) {
    return x + 1;
}
console.log(addOne(1)); // 2


// Pythonのようにclassもある
class MyClass {
    constructor(x, y) { // def __init__(self, x, y):
        this.x = x; // selfではなくthis
        this.y = y;
    }
    addX(amount) {
        this.x += amount;
    }
}
const m = new MyClass(10, 0) // newが必要
m.addX(10)
m.x === 20 && m.y === 0

// 無名関数
const addOneLambda = x => x + 1; // lambda x: x + 1
const myFunc = () => {
    console.log("Hello!");
    return 1;
}
let y = addOneLambda(1); // y === 2
myFunc();

// 関数に引数を渡さないとどうなるか => エラーを出さずに undefined が勝手に入る(結構困り者)
const mc = new MyClass()
mc.x === undefined && mc.y === undefined
mc.addX(10) // これは undefined + 10 => NaN 最悪すぎる。まだエラーを出さない
```
