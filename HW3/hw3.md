<h1>HW3</h1>

```swift
import SwiftUI

struct ContentView: View {
    var body: some View{
        
        VStack{
            TitleView()
        }
        HStack{
            ZStack{
                ZooView(imageName: "Bear")
                Text("Age:12")
                    .font(.system(size:20))
                    .fontWeight(.bold)
                    .offset(x: 30, y: 30)
                    .foregroundColor(.white)
            }
            ZStack{
                ZooView(imageName: "Cat")
                Text("Age:20")
                    .font(.system(size:20))
                    .fontWeight(.bold)
                    .offset(x: 30, y: 30)
                    .foregroundColor(.pink)
            }
            ZStack{
                ZooView(imageName: "Balloon")
                Text("age:8")
                    .font(.system(size:20))
                    .fontWeight(.bold)
                    .offset(x: 30, y: 30)
                    .foregroundColor(.blue)
            }
        }
        HStack{
            ZStack{
                ZooView(imageName: "Dog")
                Text("Age:10")
                    .font(.system(size:20))
                    .fontWeight(.bold)
                    .offset(x: 30, y: 30)
                    .foregroundColor(Color.green)
            }
            ZStack{
                ZooView(imageName: "Noodle")
                Text("Age:9")
                    .font(.system(size:20))
                    .fontWeight(.bold)
                    .offset(x: 30, y: 30)
                    .foregroundColor(.white)
            }
            ZStack{
                ZooView(imageName: "Bear2")
                Text("Age:82")
                    .font(.system(size:20))
                    .fontWeight(.bold)
                    .offset(x: 30, y: 30)
                    .foregroundColor(.white)
            }
        }
        HStack{
            ZStack{
                ZooView(imageName: "Duck")
                Text("Age:3")
                    .font(.system(size:20))
                    .fontWeight(.bold)
                    .offset(x: 30, y: 30)
                    .foregroundColor(.black)
            }
            ZStack{
                ZooView(imageName: "Pig")
                Text("Age:8")
                    .font(.system(size:20))
                    .fontWeight(.bold)
                    .offset(x: 30, y: 30)
                    .foregroundColor(.cyan)
            }
            ZStack{
                ZooView(imageName: "Dog2")
                Text("Age:11")
                    .font(.system(size:20))
                    .fontWeight(.bold)
                    .offset(x: 30, y: 30)
                    .foregroundColor(.black)
            }
        }
    }
}


struct TitleView: View {
    var body: some View{
        VStack(alignment:.center, spacing:2){
            Text("Jeffrey's")
                //.cornerRadius(30, antialiased: true)
                //.background(Color.brown)
                .font(.system(size:30))
            Text("Zoo")
                .font(.title)
                .foregroundColor(Color(red: 29 / 255, green: 40 / 255, blue: 192 / 255))
        }
    }
}
struct BearView: View{
    var body : some View{
        VStack{
            Image("Bear")
                .resizable()
                .aspectRatio(contentMode:.fit)
                .frame(width: UIScreen.screenWidth/3-250, alignment:.center)
            Text("Bear")
                .fontWeight(.bold)
                .font(.system(size:30))
        }
    }
}

struct CatView: View {
    var body: some View{
        VStack{
            Image("Cat")
                .resizable()
                .aspectRatio(contentMode: .fit)
                .frame(width: UIScreen.screenWidth/3-250,alignment: .center)
            Text("Cat")
                .fontWeight(.bold)
                .font(.system(size:30))
        }.padding(.all, 2)
    }
}

struct DogView: View{
    var body: some View{
        VStack{
            Image("Dog")
                .resizable()
                .aspectRatio(contentMode:.fit)
                .padding(.all,15)
            Text("Dog")
                .fontWeight(.bold)
                .font(.system(size:30))
        }
    }
}
struct ZooView: View{
    var imageName:String
    var body: some View{
        VStack{
            Image(imageName)
                .resizable()
                .aspectRatio(contentMode: .fit)
                .frame(width: 200 ,alignment: .center)
            Text(imageName.capitalized)
                .fontWeight(.bold)
                .font(.system(size:25))
        }.frame(minWidth: 0, idealWidth: 100, maxWidth: .infinity, minHeight: 0, idealHeight: 100, maxHeight: .infinity, alignment: .center)
    }
}
//struct TextView: View{
//    var textAge: String
//    var body: some view{
//        Text("Age:"+textAge)
//    }
//}
extension UIScreen{
    static let screenWidth = UIScreen.main.bounds.size.width
    static let screenHeight = UIScreen.main.bounds.size.height
    static let screenSize = UIScreen.main.bounds.size
}
```
<img src="https://raw.githubusercontent.com/BurningBeans/yzu-swiftui-1121-1093508/main/HW3/IMG_0214.PNG">
