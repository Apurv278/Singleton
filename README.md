# Singleton

package com.example.pappu.singleton_demo;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

import java.util.Locale;

public class MainActivity extends AppCompatActivity {

  /*  public class bubble{
        private static final int Add_MOre_Button =10;
        private int nobubble;

        public int getNobubble() {
            return nobubble;
        }
        public void addMoreButton(){
            nobubble += Add_MOre_Button*/
 //       }

//    }







    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        setupAddmoreButton();
        setupPopBubble();
        

    }

    @Override
    protected void onResume() {
        super.onResume();
        updateUI();
    }

    private void updateUI() {
        TextView txt = findViewById(R.id.textView);
        String msg = String.format(Locale.getDefault(), "%d bubbles left!", 10);
        txt.setText(msg);
    }

    private void setupPopBubble() {
        Button btn = findViewById(R.id.bubble);
        btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // bubble.AddMoreButton();
                updateUI();
            }
        });
    }

    private void setupAddmoreButton() {
        Button btn = findViewById(R.id.start);
        btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

            }
        });
    }
}
