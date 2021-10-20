# github.com/JonnyGamer/Grids/

```
class Hexagon: SKShapeNode {
    static func Create() -> Hexagon {
        let amount = 6
        var ppppoints: [CGPoint] = []
        let PI = 3.141592653
        for i in 0...amount {
            let theta = Double(i)*2.0*PI / Double(amount); // angle to the ith vertex, in radians (not degrees)
            let x = 50 * cos(theta)
            let y = 50 * sin(theta)
            let vertex = CGPoint(x: x, y: y)
            ppppoints.append(vertex)
        }
        
        let foo = Hexagon.init(points: &ppppoints, count: amount + 1)
        
        foo.fillColor = .clear
        foo.strokeColor = .gray
        return foo
    }
}
```


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

```
let c = NSColor.init(red: CGFloat((4*mandel)%255)/255, green: CGFloat((3*mandel)%255)/255, blue: CGFloat((8*mandel)%255)/255, alpha: 1.0)

```
