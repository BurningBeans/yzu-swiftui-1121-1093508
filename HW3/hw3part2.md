<h1>HW3part2</h1>

```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        VStack{
            Text("YZU雜貨店")
                .font(.system(size:50))
                .fontWeight(.bold)
                .background(.cyan)
                .cornerRadius(10.0)
            Text("3C")
                .font(.title2)
            HStack{
                ItemView(imageName: "iPhone15", price: 25880)
                ItemView(imageName: "iPhone15Pro", price: 39990)
                ItemView(imageName: "S23U", price: 30880)
                ItemView(imageName: "Charger", price: 390)
            }
            Text("Drinks")
                .font(.title2)
            HStack{
                ItemView(imageName: "Coke", price: 80)
                ItemView(imageName: "Sprite", price: 80)
                ItemView(imageName: "Coffee", price: 199)
            }
        }
        
    }
}
struct ItemView: View{
    var imageName:String
    var price:Int
    var body: some View{
        VStack{
            Image(imageName)
                .resizable()
                .aspectRatio(contentMode: .fit)
                .frame(width: 200 ,alignment: .center)
                .clipShape(.circle)
            Text(imageName.capitalized)
                .fontWeight(.bold)
                .font(.system(size:25))
            Text("$"+String(price))
        }.frame(minWidth: 0, idealWidth: 100, maxWidth: .infinity, minHeight: 0, idealHeight: 100, maxHeight: .infinity, alignment: .center)
    }
}
```
<img src="https://raw.githubusercontent.com/BurningBeans/yzu-swiftui-1121-1093508/main/HW3/IMG_0213.PNG">
