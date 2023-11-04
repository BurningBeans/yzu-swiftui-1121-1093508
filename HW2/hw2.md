<h1>HW2</h1>

```swift
import SwiftUI
enum HandShape: String{
    case rock = "✊"
    case paper = "✋"
    case scissors = "✌️"
    static func randomShape() -> HandShape{
        let shapes = ["✊", "✋", "✌️"]
        let randomShape = shapes.randomElement()!
        return HandShape(rawValue: randomShape)!
    }
    func beats(_ opponent: HandShape) -> String{
        if self == opponent{
            return "平手"
        }
        else if self == .rock && opponent == .scissors{
            return "你贏了"
        }
        else if self == .paper && opponent == .rock{
            return "你贏了"
        }
        else if self == .scissors && opponent == .paper{
            return "你贏了"
        }
        else{
            return "你輸了"
        }
    }
}
struct ContentView : View {
    @State private var computerHandShape: HandShape? = nil
    @State private var playerHandShape: HandShape? = nil
    @State private var winStatus = ""
    
    var body: some View {
        ZStack{
            Rectangle()
                .fill(Color.gray)
                .frame(minWidth: 0, idealWidth: 100, maxWidth: .infinity, minHeight: 0, idealHeight: 100, maxHeight: .infinity)
                .ignoresSafeArea(.all)
            VStack {
                Text("剪刀石頭布")
                    .font(.largeTitle)
                    .fontWeight(.heavy)
                    .padding()
                HStack {
                    Button(action: {
                        self.playerHandShape = .rock
                        self.computerHandShape = HandShape.randomShape()
                        self.winStatus = self.playerHandShape!.beats(self.computerHandShape!)
                    }) {
                        Text("✊")
                            .font(.system(size: 80))
                            .background(.red)
                            .clipShape(Circle())
                    }
                    Button(action: {
                        self.playerHandShape = .paper
                        self.computerHandShape = HandShape.randomShape()
                        self.winStatus = self.playerHandShape!.beats(self.computerHandShape!)
                    }) {
                        Text("✋")
                            .font(.system(size: 80))
                            .background(.green)
                            .clipShape(Circle())
                    }
                    Button(action: {
                        self.playerHandShape = .scissors
                        self.computerHandShape = HandShape.randomShape()
                        self.winStatus = self.playerHandShape!.beats(self.computerHandShape!)
                    }) {
                        Text("✌️")
                            .font(.system(size: 80))
                            .background(.blue)
                            .clipShape(Circle())
                    }
                }
                Text("電腦出：\(computerHandShape?.rawValue ?? "")")
                    .font(.largeTitle)
                    .fontWeight(.heavy)
                    .padding()
                Text(winStatus)
                    .font(.largeTitle)
                    .fontWeight(.heavy)
                    .padding()
            }
        }
    }
}

```
[HW2](https://raw.githubusercontent.com/BurningBeans/yzu-swiftui-1121-1093508/main/HW2/hw2.mp4)
