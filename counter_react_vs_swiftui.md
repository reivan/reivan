# Counter App in React vs SwiftUI

## React

```javascript
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <button onClick={() => setCount(count - 1)}>-</button>
      <span>{count}</span>
      <button onClick={() => setCount(count + 1)}>+</button>
    </div>
  );
}
```

## SwiftUI

```swift
import SwiftUI

struct Counter: View {
  @State private var count = 0

  var body: some View {
    HStack {
      Button(action: { self.count -= 1 }) {
        Text("-")
      }
      Text("\(count)")
      Button(action: { self.count += 1 }) {
        Text("+")
      }
    }
  }
}

```
