function calculateBMI(){

let weight=document.getElementById("weight").value
let height=document.getElementById("height").value/100

let bmi=weight/(height*height)

document.getElementById("result").innerHTML="Your BMI: "+bmi.toFixed(2)

}

function saveWorkout(){

let date=document.getElementById("date").value

let li=document.createElement("li")
li.innerText="Workout saved on "+date

document.getElementById("calendarList").appendChild(li)

}

function sendMessage(){

let input=document.getElementById("userInput").value
let chatbox=document.getElementById("chatbox")

let user=document.createElement("p")
user.innerHTML="<b>You:</b> "+input
chatbox.appendChild(user)

let bot=document.createElement("p")

if(input.includes("workout"))
bot.innerHTML="<b>FIT Bot:</b> Try pushups, squats and planks!"

else if(input.includes("bmi"))
bot.innerHTML="<b>FIT Bot:</b> Use our BMI calculator in workout page."

else
bot.innerHTML="<b>FIT Bot:</b> Stay active and drink water!"

chatbox.appendChild(bot)

}
