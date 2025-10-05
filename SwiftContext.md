```swift
@EnvironmentObject var context: SwiftContext
let hasPro = context.hasPro

VStack {
        Button(action: {
            SwiftContext.shared?.hasPro.toggle()
        }, label: {
            Text("Hi \(context.hasPro ? "Pro" : "Free") User!")
        })
}
.environmentObject(SwiftContext.create(appGroup: "group.in.hocg.app"))

```