<h1>hw1</h1>
<tabel>
  <tr>
    <td>
      <img src="https://raw.githubusercontent.com/mya2002/yzu-SwiftUI-1103304/main/imghw1.png">
```swift
      import SwiftUI
//學號，姓名，大頭照，SF simbol，你的一句話 deadline:11/06
struct ContentView: View {
    var body: some View {
        VStack {
            Image(systemName:"face.smiling")
                .font(.system(size:100))
                .foregroundColor(.green)
                .shadow(color:.gray, radius:5, x: 5, y: /*@START_MENU_TOKEN@*/0.0/*@END_MENU_TOKEN@*/)
         Text("1103304王彥雅")
                .fontWeight(/*@START_MENU_TOKEN@*/.bold/*@END_MENU_TOKEN@*/)
                .font(/*@START_MENU_TOKEN@*/.title/*@END_MENU_TOKEN@*/)
                .padding()
            Image("影像內容")
                .resizable()
                .aspectRatio(contentMode: /*@START_MENU_TOKEN@*/.fill/*@END_MENU_TOKEN@*/)
                .frame(width:200,height:200,alignment: .center)
                .background(Color.yellow)
                .clipShape(Circle())
                .opacity(/*@START_MENU_TOKEN@*/0.8/*@END_MENU_TOKEN@*/)
                .shadow(color: .gray, radius: /*@START_MENU_TOKEN@*/10/*@END_MENU_TOKEN@*/, x: 0.0, y: /*@START_MENU_TOKEN@*/0.0/*@END_MENU_TOKEN@*/)
               /* .overlay(
                    Text("ooooooo")
                        .fontWeight(.heavy)
                        .lineSpacing(20)
                        .font(.system(size:32.0))
                        .foregroundColor(.white)
                        .frame(width:350,height:150,alignment:.center)
                        .background(Color.purple)
                        .cornerRadius(30)
                        .opacity(0.8)
                    ,
                    alignment: .bottom
                )*/
                
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
    </td>
  </tr>
</tabel>
