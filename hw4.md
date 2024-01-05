<h1>Homework_4</h1>
<table>
  <tr>
    <td>
      <img src="https://raw.githubusercontent.com/mya2002/yzu-SwiftUI-1103304/main/IMG_1587.gif">
    </td>
    <td>
      
```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        VStack {
            Text("讓我爆哭的動畫")
                .font(.largeTitle)
                .fontWeight(.heavy)
                .foregroundStyle(.primary)
            TabView{
                //Group{
                    WelcomeView()
                        .tabItem {     
                            Image(systemName: "rosette")
                            Text("Welcome")
                        }
                   CourseListView()
                        .tabItem {  
                            Image(systemName: "list.dash")
                            Text("Course")
                        }
                CardView()                        
                    .tabItem { 
                            Image(systemName: "book")
                            Text("Learn")
                        }
                //}
                //.toolbarBackground(Color.black,for:.tabBar)
                //.toolbarBackground(.visible, for: .tabBar)
            }
            //.tint(.yellow)
        }
    }
}
struct TermAndDescription:Identifiable{
    var id = UUID()
    var term:String
    var description:String
}

var myDictionary = [
    TermAndDescription(term:"R2 Score",description: "1"),
    TermAndDescription(term:"R2 Score",description: "2"),
    TermAndDescription(term:"R2 Score",description: "3"),
    TermAndDescription(term:"R2 Score",description: "4")
]

struct CardView:View{
    @State var currentCard = 0
    var body: some View{
        VStack{
            VStack{
                Text(myDictionary[currentCard].term)
                    .font(.title)
                    .padding(.all,10)
                Text(myDictionary[currentCard].description)
                    .font(.body)
                    .foregroundColor(/*@START_MENU_TOKEN@*/.blue/*@END_MENU_TOKEN@*/)
                    .padding(.all,10)
            }
            .frame(minWidth:0,idealWidth:100,maxWidth:300,minHeight: 0,idealHeight: 100,maxHeight: 300,alignment: .center)
            .background(Color.yellow)
            .onTapGesture {
                if currentCard<myDictionary.count-1{
                    currentCard+=1
                }else{
                    currentCard=0
                }
            }
            Text("點擊看下一張")
                .padding(.all,10)
        }
    }
}
struct Course:Identifiable{
    var id=UUID()
    var name:String
    var image:String
    var description:String
}

var courses = [
    Course(name:"進擊的巨人",image:"進擊的巨人",description: "全93集"),
    Course(name:"暗殺教室",image:"暗殺教室",description: "全47集"),
    Course(name:"未聞花名",image:"未聞花名",description: "全13集"),
    Course(name:"刀劍神域",image:"刀劍神域",description: "全48集"),
    Course(name:"來自風平浪靜的明日",image:"風平浪靜",description: "全26集")
    
]

struct BasicImageRow:View{
    var thisCourse:Course
    var body:some View{
        HStack{
            Image(thisCourse.image)
                .resizable()
                .frame(width:40,height:40)
                .cornerRadius(5)
            Text(thisCourse.name)
        }
    }
}

struct CourseDetailView:View{
    @Environment(\.presentationMode) var presentationMode
    var thisCourse:Course
    var body: some View{
        ScrollView{
            VStack{
                Image(thisCourse.image)
                    .resizable()
                    .aspectRatio(contentMode:.fill)
                    .clipped()
                Text(thisCourse.name)
                    .font(.system(.title, design: .rounded))
                    .fontWeight(.black)
                Spacer()
                Text(thisCourse.description)
                    .font(.system(.subheadline,design: .rounded))
                    .fontWeight(.light)
                Spacer()
            }
        }
        .overlay(
        HStack{
            Spacer()
            VStack{
                Button(action:{
                    self.presentationMode.wrappedValue.dismiss()
                },label: {
                    Image(systemName: "chevron.down.circle.fill")
                        .font(.largeTitle)
                        .foregroundColor(.white)
                })
                .padding(.trailing,20)
                .padding(.top,40)
                Spacer()
            }
        }
        )
    }
}

struct CourseListView:View{
    @State var showDetailView = false
    @State var selectedCourse:Course?
    var body: some View{
        NavigationView{
            List(courses){ courseItem in
                BasicImageRow(thisCourse: courseItem)
                    .onTapGesture {
                        self.showDetailView = true
                        self.selectedCourse = courseItem
                    }
            }
            .sheet(item:self.$selectedCourse){ thisCourse in
                CourseDetailView(thisCourse:thisCourse)
            }
            .navigationBarTitle("動畫列表")
        }
    }
}
struct WelcomeView:View{
    var body:some View{
        VStack{
            Image("cry")
                .resizable()
                .aspectRatio( contentMode: .fit)
            Text("還沒看過\n一定要快點補上")
                .fontWeight(.heavy)
                .lineSpacing(20)
                .font(.system(size:32.0))
                .foregroundColor(.white)
                .frame(width:350,height:150,alignment: .center)
                .background(Color.blue)
                .cornerRadius(20.0)
                .multilineTextAlignment(.center)
        }
    }
}

```
    
  </tr>
</table>
