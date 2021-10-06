# github.com/JonnyGamer/Grids/

```swift
func mandelBrotSet(c: (r: Double, i: Double), MAX_ITERATIONS: Int = 1000) -> Int {
        var m = (r: 0.0, i: 0.0); // m for Mandelbrot :)

        for i in 0..<MAX_ITERATIONS {
            let temp = m.r;
            m.r = (m.r * m.r) - (m.i * m.i) + c.r;
            m.i = 2 * temp * m.i + c.i;
          if (m.r * m.r + m.i * m.i > 4) {
              return i;
          }
            
        }
        return MAX_ITERATIONS-1
        
    }
```
