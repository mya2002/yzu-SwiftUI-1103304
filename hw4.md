<h1>Homework_1</h1>
<table>
  <tr>
    <td>
      <img src="https://raw.githubusercontent.com/mya2002/yzu-SwiftUI-1103304/main/imghw1.png">
    </td>
    <td>
      
```swift
import SwiftUI
//學號，姓名，大頭照，SF simbol，你的一句話 deadline:11/06
struct ContentView: View {
    var body: some View {
        VStack {
            Image(systemName:"face.smiling")
                .font(.system(size:100))
                .foregroundColor(.green)
                .shadow(color:.gray, radius:5, x: 5, y:0.0)
         Text("1103304王彥雅")
                .fontWeight(.bold)
                .font(.title)
                .padding()
            Image("影像內容")
                .resizable()
                .aspectRatio(contentMode: .fill)
                .frame(width:200,height:200,alignment: .center)
                .background(Color.yellow)
                .clipShape(Circle())
                .opacity(0.8)
                .shadow(color: .gray, radius: 10, x: 0.0, y:0.0)
            Text("I'm the one I should love in the world.")
                .fontWeight(.heavy)
                .lineSpacing(10)
                .font(.system(size:16))
                .foregroundColor(.white)
                .frame(width:350,height:150,alignment:.center)
                .background(Color.purple)
                .cornerRadius(30)
                .opacity(0.8)
        }
    }
}
```
    
  </tr>
</table>
