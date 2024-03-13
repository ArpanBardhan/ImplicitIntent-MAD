# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
```
Step 1: Open Android Stdio and then click on File -> New -> New project.
Step 2: Then type the Application name as ImplicitIntent and click Next.
Step 3: Then select the Minimum SDK as shown below and click Next.
Step 4: Then select the Empty Activity and click Next. Finally click Finish.
Step 5: Design layout in activity_main.xml.
Step 6: Display message give in MainActivity file.
Step 7: Save and run the application.
```

## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: ARPAN BARDHAN
Registeration Number : 212222040013
*/
```

activity_main.xml
```XML
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView2"
        android:layout_width="220dp"
        android:layout_height="83dp"
        android:text="Implict Intent"
        android:textSize="34sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.507"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.083" />

    <EditText
        android:id="@+id/editTextText"
        android:layout_width="298dp"
        android:layout_height="67dp"
        android:ems="10"
        android:inputType="text"
        android:text="Name"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.575"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView2"
        app:layout_constraintVertical_bias="0.065" />

    <Button
        android:id="@+id/button"
        android:layout_width="223dp"
        android:layout_height="68dp"
        android:text="Click Me"
        android:textSize="34sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.515"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView2"
        app:layout_constraintVertical_bias="0.498" />
</androidx.constraintlayout.widget.ConstraintLayout>
```

MainActivity.java
```java
package com.example.implicitindent;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        Button button;
        EditText editText;
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        //Intent intent = new Intent(Intent.ACTION_VIEW);
        //intent.setData(Uri.parse("https://www.geeksforgeeks.org/"));
        //startActivity(intent);
        button = findViewById(R.id.button);
        editText = (EditText) findViewById(R.id.editTextText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url = editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });

    }
}
```

## OUTPUT
![Screenshot (437)](https://github.com/ArpanBardhan/ImplicitIntent-MAD/assets/119405037/0431d419-e2d0-43d2-88c3-b3adfa3d8b57)

![Screenshot (439)](https://github.com/ArpanBardhan/ImplicitIntent-MAD/assets/119405037/9eeaf559-11e8-4624-a499-54a47d8ee963)

![Screenshot (440)](https://github.com/ArpanBardhan/ImplicitIntent-MAD/assets/119405037/c79bd036-4257-4352-b396-e7aa43d72c35)




## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


