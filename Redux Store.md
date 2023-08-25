![[Pasted image 20230811063120.png]]

```js
import { createStore } from "redux";

const CAKE_ORDERED = "CAKE_ORDERED";

function orderCake() {
  return {
    type: CAKE_ORDERED,
    quantity: 1,
  };
}

const initialState = {
  numberOfCakes: 10,
};

const reducer = (state = initialState, action) => {
  switch (action.type) {
    case CAKE_ORDERED:
      return {
        ...state,
        numberOfCakes: state.numberOfCakes - action.quantity,
      };
    default:
      return state;
  }
};

const store = createStore(reducer);
console.log(`Initial Store: `, store.getState());

const unsubscribe = store.subscribe(() =>
  console.log("Updated state:", store.getState())
);

store.dispatch(orderCake());
store.dispatch(orderCake());
store.dispatch(orderCake());

unsubscribe();

```
