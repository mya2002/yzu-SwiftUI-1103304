<h1>Homework_3</h1>
<table>
  <tr>
    <td>
      <img src="https://raw.githubusercontent.com/mya2002/yzu-SwiftUI-1103304/main/imghw3.png">
    </td>
    <td>
      
```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        VStack {
            TitleView()
            HStack{
                vaseView()
                trophyView()
            }
                VStack{
                    HStack{
                        FruitView(imageName: "Bear")
                        FruitView(imageName: "Bear2")
                        FruitView(imageName: "Bear3")
                    }
                    FishView()
                }
        }
    }
}
struct TitleView: View{
    var body: some View {
        VStack (alignment: .center, spacing: 2){
            Text("Mya的")
                .font(.system(size:30))
            Text("櫃子")
                .font(.title)
                .foregroundColor(Color(red:29/255,green:40/255,blue:192/255))
        }
    }
}
struct vaseView: View{
    var body: some View {
        VStack (alignment: .center, spacing: 2){
            Image("Vase")
                .resizable()
                .aspectRatio(contentMode:.fit)
                .frame(width: 150,
                       alignment:.center)
            Text("Vase")
                .fontWeight(.bold)
                .font(.system(size:30))
        }
    }
}
struct trophyView: View{
    var body: some View {
        VStack (alignment: .center, spacing: 2){
            Image("Trophy")
                .resizable()
                .aspectRatio(contentMode:.fit)
                .frame(width: 159,
                       alignment:.center)
            Text("trophy")
                .fontWeight(.bold)
                .font(.system(size:30))
        }
    }
}
struct FruitView:View{
    var imageName:String
    var body: some View{
        VStack{
            Image(imageName)
                .resizable()
                .aspectRatio(contentMode:.fit)
                .frame(height:100,alignment:.center)
            //.capitalized = 首字大寫
            Text(imageName.capitalized)
                .fontWeight(.bold)
                .font(.system(size:25))
        }
    }
}
struct FishView: View{
    var body: some View {
        VStack (alignment: .center, spacing: 2){
            Image("Book")
                .resizable()
                .aspectRatio(contentMode:.fit)
                .frame(width: 300,
                       alignment:.center)
            Text("Book")
                .fontWeight(.bold)
                .font(.system(size:30))
        }
    }
}
extension UIScreen{
    static let screenWidth = UIScreen.main.bounds.size.width
    static let screenHeight = UIScreen.main.bounds.size.height
    static let screenSize = UIScreen.main.bounds.size
}
```
    
  </tr>
</table>
