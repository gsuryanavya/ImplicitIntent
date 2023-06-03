# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step1:Open Android Studio and create a new project.

Step2:In the activity_main.xml file, design the layout with a TextInputEditText element for the text field and a Button element for the "Navigate" button.

Step3:In the MainActivity.java file, retrieve references to the text field and the button using their IDs.

Step4:Set an OnClickListener for the button.

Step5:Inside the OnClickListener, retrieve the text entered in the text field using the getText() method.

Step6:Create an Intent object to open a web page with the URL obtained from the text field.

Step7:Set the action of the intent to Intent.ACTION_VIEW to indicate that the intent is used for viewing something.

Step8:Set the data of the intent to the URL obtained from the text field using the Uri.parse() method.

Step9:Set the type of the intent to "text/html" or "text/plain" to specify the type of data being viewed.

Step10:Use the startActivity() method with the intent to start the activity that can handle the implicit intent.

Step11:Run the application on an Android device or emulator to see the desired functionality.


## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by:Golla Navya
Registeration Number :212221040048
*/
```
## Activity_main.xml:
```
Activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity">
 <EditText
 android:id="@+id/editText"
 android:layout_width="267dp"
 android:layout_height="75dp"
 android:ems="10"
 android:inputType="textPersonName"
 android:hint="Enter your name"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.497"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.412" />
 <Button
 android:id="@+id/button"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="Button"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.498"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.519" />
</androidx.constraintlayout.widget.ConstraintLayout>

```
## MainActivtiy.java:
```
MainActivtiy.java:
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
public class MainActivity extends AppCompatActivity {
 Button button;
 EditText editText;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 button = findViewById(R.id.button);
 editText = findViewById(R.id.editText);
 button.setOnClickListener(view -> {
 String url = editText.getText().toString();
 Intent intent = new Intent(Intent.ACTION_VIEW, 
Uri.parse(url));
 startActivity(intent);
 });
 }
}
```

## OUTPUT
![WhatsApp Image 2023-06-03 at 23 20 02](https://github.com/gsuryanavya/ImplicitIntent/assets/133086963/4e63b089-82b7-4897-8709-9d4735612939)
![WhatsApp Image 2023-06-03 at 23 20 12](https://github.com/gsuryanavya/ImplicitIntent/assets/133086963/78e2af76-05b2-43e3-8cab-144ff90b782a)




## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.
