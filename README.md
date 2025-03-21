void setup()
{
     pinMode(5, OUTPUT);
     pinMode(6, OUTPUT);
     pinMode(9, OUTPUT);
     pinMode(10, OUTPUT);
}

void forward(int t)
{
     digitalWrite(6, 1);
     digitalWrite(10, 1);
     digitalWrite(5, 0);
     digitalWrite(9, 0);
     delay(t/16);
}

void backward(int t)
{
     digitalWrite(6, 0);
     digitalWrite(10, 0);
     digitalWrite(5, 1);
     digitalWrite(9, 1);
     delay(t/16);
}

void stop(int t)
{
     digitalWrite(6, 0);
     digitalWrite(10, 0);
     digitalWrite(5, 0);
     digitalWrite(9, 0);
     delay(t/16);
}

void left(int t)
{
     digitalWrite(6, 1);
     digitalWrite(10, 0);
     digitalWrite(5, 0);
     digitalWrite(9, 1);
     delay(t/16);
}

void right(int t)
{
     digitalWrite(6, 0);
     digitalWrite(10, 1);
     digitalWrite(5, 1);
     digitalWrite(9, 0);
     delay(t/16);
}

void loop()
{
     forward(2000);
     stop(250);
     backward(2000);
     stop(250);
     left(2000);
     stop(250);
     right(2000);
     stop(250);
}
