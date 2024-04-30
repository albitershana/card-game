import SwiftUI
struct ContentView: View {
 // all variable initializations
@State private var card1:String = "card1"
@State private var card2:String = "card2"
@State private var card3:String = "card3"
@State private var card4:String = "card4"
@State private var value4:Int = 0
@State private var value3:Int = 0
@State private var value2:Int = 0
@State private var value1:Int = 0
@State private var frequency:Int = 0
@State private var highPos:String = ""
@State private var lowPos:String = ""
@State private var range:Int = 0
@State private var average:Int = 0
@State private var sum:Int = 0
@State private var high:String = ""
@State private var low:String = ""
@State private var lowValue:Int = 0
@State private var highValue:Int = 0
@State private var resultMessage:String = ""
 
 var body: some View {
 VStack {
 HStack {
 Image(card1)
 .resizable()
 
 Image(card2)
 .resizable()
 } // end HStack
 
 HStack {
 Image(card3)
 .resizable()
 
 Image(card4)
 .resizable()
 } // end HStack
 
 Button(action: {
 var randomNumber:Int = 0
 for i in 1...4 {
 // randomizer for cards
if i == 1 {
 randomNumber = Int.random(in: 1...13)
 card1 = "card" + String(randomNumber)
 value1 = randomNumber

 }
 else if i == 2 {
 randomNumber = Int.random(in: 1...13)
 card2 = "card" + String(randomNumber)
value2 = randomNumber
 }
 else if i == 3 {
 randomNumber = Int.random(in: 1...13)
 card3 = "card" + String(randomNumber)
value3 = randomNumber
 }
 else if i == 4 {
 randomNumber = Int.random(in: 1...13)
 card4 = "card" + String(randomNumber)
     value4 = randomNumber
 }
    // high value calculator
     if value1 >= value2 && value1 >= value3 && value1 >= value4 {
             high = card1
         highValue = value1
         highPos = "High Position: 1"
         } else if value2 >= value1 && value2 >= value3 && value2 >= value4 {
             high = card2
            highValue = value2
             highPos = "High Position: 2"
         } else if value3 >= value1 && value3 >= value2 && value3 >= value4 {
             high = card3
             highValue = value3
             highPos = "High Position: 3"
         } else {
             high = card4
             highValue = value4
             highPos = "High Position: 4"
         }
     // low value calculator
     if value1 <= value2 && value1 <= value3 && value1 <= value4 {
             low = card1
         lowValue = value1
         lowPos = "Low Position: 1"
         } else if value2 <= value1 && value2 <= value3 && value2 <= value4 {
             low = card2
             lowValue = value2
             lowPos = "Low Position: 2"
         } else if value3 <= value1 && value3 <= value2 && value3 <= value4 {
             low = card3
             lowValue = value3
             lowPos = "Low Position: 3"
         } else {
             low = card4
             lowValue = value4
             lowPos = "Low Position: 4"
         }
     // math calculations
     range = highValue - lowValue
     sum = value1 + value2 + value3 + value4
     average = sum / 4
     // frequency calculator
     if value1 == value2 && value1 == value3 && value1 == value4 {
                     frequency = value1
                 } else if value1 == value2 && value1 == value3 {
                     frequency = value1
                 } else if value1 == value2 && value1 == value4 {
                     frequency = value1
                 } else if value1 == value3 && value1 == value4 {
                     frequency = value1
                 } else if value2 == value3 && value2 == value4 {
                     frequency = value2
                 } else if value1 == value2 || value1 == value3 || value1 == value4 {
                     frequency = value1
                 } else if value2 == value3 || value2 == value4 {
                     frequency = value2
                 } else if value3 == value4 {
                     frequency = value3
                 } else {
                     frequency = 0
                 }
     resultMessage = "High Card: \(high) Low Card: \(low) Sum: \(sum) Freq(Most): \(frequency) \(highPos) \(lowPos) Average: \(average) Range: \(range)"  } // end for loop
      }, label:{
      Text("RANDOM")
      .padding()
      .foregroundColor(Color.green)
      .font(.largeTitle)
      
      }) // end button
      
      Text(resultMessage)
      .frame(width: 350, height: 80, alignment: .leading)
      .background(Color.white)
      .foregroundColor(Color.black)
      
      } // end VStack
      
      } // end body
      
     } // end struct
     struct ContentView_Previews: PreviewProvider {
      static var previews: some View {
      ContentView()
      }
     }
