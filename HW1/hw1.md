<h1>HW1</h1>

```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        Text("1093508\t\t沈泰宏")
            .font(.title)
            .padding(.top)
            .foregroundColor(Color.mint)
        Image("Img")
            .resizable()
        //.scaledToFit()
        //.font(.system(size:100))
            .aspectRatio(contentMode:.fit)
            .frame(width:300, height:400,
                   alignment:.center)
            .clipShape(Circle())
            .overlay(
                Image(systemName: "heart.fill")
                    .foregroundColor(.red)
                    .font(.system(size:50))
                    .opacity(0.75)
                    .frame(width:200,height:275,alignment:.top
                      )
            .overlay(
                Text("Hello World!")
                    .font(.system(size:24))
                    .fontWeight(.heavy)
                    .frame(width:200,height:30,alignment: .center)
                    .foregroundColor(.white)
                    .background(Color.cyan)
                    .cornerRadius(15.0, antialiased: true)
                    .opacity(0.8)
                    ,alignment: .bottom
                    )
            )
    }
}
```