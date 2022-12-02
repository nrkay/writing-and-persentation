## PENGGUNAAN PROPTYPES

Dalam permograman kita mungkin mendapatkan bugs yang mengharuskan kita untuk menge-cek tipe data. React memiliki kemampuan pengecekan tipe data menggunakan

```
import PropTypes from 'prop-types'
```

contoh penggunaanya :

```
import PropTypes from 'prop-types';

class Greeting extends React.Component {
  render() {
    return (
      <h1>Hello, {this.props.name}</h1>
    );
  }
}

Greeting.propTypes = {
  name: PropTypes.string
};
```

## PENGGUNAAN ROUTER

cara penggunaan router :

1. Install package/library

```
npm install react-router-dom@6
```

2. Import pada main.js

```
import { BrowserRouter } from "react-router-dom";
```

3. Pada main.js, bungkus App.js dengan BrowserRouter

```
<BrowserRouter>
```

4. Pada App.js, import

```
import { Routes, Route, Link } from "react-router-dom";
```

5. Penggunaan Routes menggunakan double tag Routes, yang memiliki single tag Route. Contoh

```
      <Routes>
      <Route path='/' from={<Home />} />
      </Route>
```

## STATE MANAGEMENT REACT REDUX

Alur mengerjakan redux:

1. Buat Store
2. Buat Reducer
3. Tambahkan Provider
4. Ambil data dari Store
5. Tambahkan dispatch(action)
