# ステップ3：Reactの基礎

このステップでは、Reactの最も基本的な概念である「コンポーネント」「state」「useEffect」について、実際に手を動かしながら学びます。

---

## 目標

- Reactの関数コンポーネントの書き方を理解する
- state（useState）の使い方を体験する
- useEffectの基本的な使い方を知る
- 画面に「Hello World」を表示する

---

## 1. 画面に「Hello World」を表示

1. `src/App.jsx`（または`App.js`）を開き、以下のように編集します。

    ```jsx
    function App() {
      return (
        <div>
          Hello World
        </div>
      );
    }

    export default App;
    ```

2. ブラウザで「Hello World」と表示されていればOKです。

---

## 2. useStateで状態を管理してみる

1. カウントアップボタンを追加してみましょう。

    ```jsx
    import { useState } from 'react';

    function App() {
      const [count, setCount] = useState(0);

      return (
        <div>
          <p>カウント: {count}</p>
          <button onClick={() => setCount(count + 1)}>
            +1
          </button>
        </div>
      );
    }

    export default App;
    ```

2. ボタンを押すたびにカウントが増えれば成功です。

---

## 3. useEffectの超基本

1. 画面が表示されたときに一度だけコンソールにメッセージを出してみましょう。

    ```jsx
    import { useState, useEffect } from 'react';

    function App() {
      const [count, setCount] = useState(0);

      useEffect(() => {
        console.log('コンポーネントがマウントされました');
      }, []);

      return (
        <div>
          <p>カウント: {count}</p>
          <button onClick={() => setCount(count + 1)}>
            +1
          </button>
        </div>
      );
    }

    export default App;
    ```

2. ブラウザの開発者ツールのコンソールに「コンポーネントがマウントされました」と表示されればOKです。

---

## 補足

- useStateは「状態（値）」を管理するためのReactのフックです。
- useEffectは「副作用（APIリクエストや初期化処理など）」を扱うためのフックです。
- まずは「Hello World」→「カウントアップ」→「useEffectでconsole.log」の順に体験しましょう。

---

## 参考

- [React公式ドキュメント（日本語）](https://ja.react.dev/)
- [useState](https://ja.react.dev/reference/react/useState)
- [useEffect](https://ja.react.dev/reference/react/useEffect) 