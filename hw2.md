<h1>Homework_2</h1>
<table>
  <tr>
    <td>
      <video src="https://raw.githubusercontent.com/mya2002/yzu-SwiftUI-1103304/main/video2.mov"></video>
    </td>
    <td>
      
```swift
import SwiftUI

struct ContentView: View {
    @State var randomList = ["布","剪刀","石頭"]
    @State var randomImg = ["Paper","scissor","stone"]
    @State var randomInt = Int.random(in: 0...2)
    @State var ourInt = 0
    @State var gameTimes: Int = 1
    @State var ruleName: String = "遊戲選單"
    @State var ourPoint: Int = 0
    @State var pcPoint: Int = 0
    var body: some View {
        VStack {
        Image(randomImg[randomInt])
            .resizable()
            .aspectRatio(contentMode: .fill)
            .frame(width:100,height:100,alignment: .center)
            .background(Color.yellow)
            .clipShape(Circle())
            .opacity(0.8/)
            .shadow(color: .gray, radius: 10, x: 0.0, y:0.0)
        if ourInt == 1{
            if ourInt>randomInt{
                Text("你贏了")
                    .padding(.all,10)
                    .frame(width:150,height:120,alignment: .center)
                    .font(.system(size: 40))
            }else if ourInt<randomInt{
                Text("你輸了")
                    .padding(.all,10)
                    .frame(width:150,height:120,alignment: .center)
                    .font(.system(size: 40))
            }else{
                Text("平手")
                    .padding(.all,10)
                    .frame(width:150,height:120,alignment: .center)
                    .font(.system(size: 40))
            }
        }else if ourInt == 0{
            if randomInt==2{
                Text("你贏了")
                    .padding(.all,10)
                    .frame(width:150,height:120,alignment: .center)
                    .font(.system(size:40))
            }else if randomInt==1{
                Text("你輸了")
                    .padding(.all,10)
                    .frame(width:150,height:120,alignment: .center)
                    .font(.system(size: 40))
            }else{
                Text("平手")
                    .padding(.all,10)
                    .frame(width:150,height:120,alignment: .center)
                    .font(.system(size: 40))
            }
        }else{
            if randomInt==1{
                Text("你贏了")
                    .padding(.all,10)
                    .frame(width:150,height:120,alignment: .center)
                    .font(.system(size: 40))
            }else if randomInt==0{
                Text("你輸了")
                    .padding(.all,10)
                    .frame(width:150,height:120,alignment: .center)
                    .font(.system(size: 40))
            }else{
                Text("平手")
                    .padding(.all,10)
                    .frame(width:150,height:120,alignment: .center)
                    .font(.system(size: 40))
            }
        }
        Image(randomImg[ourInt])
            .resizable()
            .aspectRatio(contentMode: .fill)
            .frame(width:100,height:100,alignment: .center)
            .background(Color.yellow)
            .clipShape(Circle())
            .opacity(0.8)
            .shadow(color: .gray, radius: 10, x: 0.0, y: 0.0)
        Button(action:{
            self.ourInt = 2
            self.randomInt = Int.random(in: 0...2)
        },label:{
            Text("石頭")
                .padding(.all,10)
                .frame(width:300,height:100,alignment: .center)
                .font(.system(size: 50))
                .background(Color.pink)
                .foregroundColor(.white)
                .cornerRadius(20)
        })
        Button(action:{
            self.ourInt=1
            self.randomInt = Int.random(in: 0...2)
        },label:{
            Text("剪刀")
                .padding(.all,10)
                .frame(width:300,height:100,alignment: .center)
                .font(.system(size: 50))
                .background(Color.purple)
                .foregroundColor(.white)
                .cornerRadius(20)
        })
        Button(action:{
            self.ourInt=0
            self.randomInt = Int.random(in: 0...2)
        },label:{
            Text("布")
                .padding(.all,10)
                .frame(width: 300, height: 100, alignment: .center)
                .font(.system(size: 50))
                .background(Color.pink)
                .foregroundColor(.white)
                .cornerRadius(20)
           })
        }
    }
}
```

  </td>
  </tr>
</table>
