# GetMealz
![logo](https://github.com/user-attachments/assets/10d86479-49e1-4c99-8654-b9979bdb0719)


#package com.example.getmealz

import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.background
import androidx.compose.foundation.layout.Column
import androidx.compose.foundation.layout.Row
import androidx.compose.foundation.layout.Spacer
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.foundation.layout.size
import androidx.compose.material3.Button
import androidx.compose.material3.HorizontalDivider
import androidx.compose.material3.OutlinedTextField
import androidx.compose.material3.Text
import androidx.compose.runtime.getValue
import androidx.compose.runtime.mutableStateOf
import androidx.compose.runtime.remember
import androidx.compose.runtime.setValue
import androidx.compose.ui.Alignment
import androidx.compose.ui.Alignment.Companion.BottomStart
import androidx.compose.ui.Modifier
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.layout.HorizontalAlignmentLine
import androidx.compose.ui.layout.layoutId
import androidx.compose.ui.text.font.FontFamily
import androidx.compose.ui.text.font.FontWeight
import androidx.compose.ui.unit.dp
import androidx.compose.ui.unit.sp
import org.intellij.lang.annotations.JdkConstants.HorizontalAlignment


class MainActivity : ComponentActivity(){

override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {


            var time_of_day by remember {
                mutableStateOf(value = "")
            }

            var meal_suggested by remember {
                mutableStateOf(value = "")
            }





            Column(
                horizontalAlignment = Alignment.CenterHorizontally,
                modifier = Modifier
                    .fillMaxSize()
                    .background(Color(0xFFC7B8EA))
            ) {
                Text(text="GetMealz",
                    fontWeight = FontWeight.Black,
                    fontSize = 50.sp,
                    fontFamily = FontFamily.Cursive



                )

                Spacer(modifier = Modifier.size(10.dp))

                Text(text = "Welcome to GetMealz, where you are guaranteed the best meal suggestions daily.")


                HorizontalDivider()
                Spacer(modifier = Modifier.size(80.dp))


                OutlinedTextField(
                    value = time_of_day,
                    onValueChange = { text ->
                        time_of_day = text
                    },
                    placeholder = { Text(text = "Enter the time of the day e.g. Morning") }

                )
                Spacer(modifier = Modifier.size(50.dp))

                Row {
                    Button(onClick = {
                        meal_suggested = when (time_of_day) {
                            "Morning" -> "Option 1: Avocado Toast Recipe\n Option 2: Cereal\n Option 3: English Breakfast"
                            "Mid-morning" -> "Option 1: Fresh Fruit Salad\n Option 2: Nuts and Seeds\n Option 3: Smoothie"
                            "Afternoon" -> "Option 1: Grilled Chicken Wrap\n Option 2: Toasted Ham and Cheese \n Option 3: Tomato Soup with bread"
                            "Mid-Afternoon" -> "Option 1: Chocolate\n Option 2: Slice of Cake\n Option 3: Fresh Fruit"
                            "Dinner" -> "Option 1: Spaghetti Bolognese\n Option 2: Beef Stew with rice\n Option 3: Grilled Chicken with Roasted Vegetables"
                            "After Dinner" -> "Option 1: Brownies\n Option 2: Malva Pudding\n Option 3: Panna Cotta"
                            else -> "invalid time of the day! Try again Remember to begin with Capital letters"
                        }
                    }) {
                        Text(text = "Suggest Meal")
                    }
                    Spacer(modifier = Modifier.size(50.dp))
                    Button(onClick = {
                        time_of_day = ""
                        meal_suggested = ""
                    }) {
                        Text(text = "Reset")
                    }

                }
                Spacer(modifier = Modifier.size(30.dp))
                Text(
                    text = "Meals suggested:",
                    fontSize = 22.sp,
                    fontWeight = FontWeight.Black
                )
                Spacer(modifier = Modifier.size(15.dp))
                Text(text = " $meal_suggested")

                Spacer(modifier = Modifier.size(255.dp))
                HorizontalDivider()

                Text(text =
                        "Time Guide\nMorning: 6:00AM - 12:00PM\nMid-morning: 10:00AM - 11:30\n Afternoon: 12:00AM - 5:00PM\n Mid-afternoon: 2:30PM - 4:00PM\n Dinner: 6:00PM - 8:00PM\nAfter dinner: 8:00PM - 10:00PM")





            }

        }
    }


    }
    Report:
    This app is called GetMealz its main purpose is to suggest maeals for users who struggle with deciding what to it,
    however this meal also serves as a diet app as it provides suggestions that are considered healthy.To make sure that 
    not only are the users fed but healthy too.
    The app is fairly straight forward this why obtained by not adding to much UI, which could easily confuse potential users of all ages. Error message is included too to assist user if invalid input has been entered. Average English has been used to accomodate people of all literature levels. Lastly Github has been used to manage bugs, feature requests and tasks, including the tracking of code changes.










    
Youtube link: https://youtu.be/SH18KZ4kNRQ?si=TlrkbBV8qpfXqbaM
GitHub: https://github.com/AyolaC/GetMealz33
