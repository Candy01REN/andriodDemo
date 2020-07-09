# andriodDemo
第一个安卓练习
第一次接触安卓开发，这是我用Andrid Studio做的第一个demo。
简单的实现了按按钮数字加倍的效果
主要实现目录是在java目录下的第一个包里的MainActivity中
fab.setOnClickListener(new View.OnClickListener() {
     @Override
     public void onClick(View view) {
         //以下五行自己实现的数字加倍
         TextView textValue=findViewById(R.id.text_value);//获取对应id的值
         String textString=textValue.getText().toString();//获取数字并转换成字符串的形式
         int originalValue=Integer.parseInt(textString);//把string值转换成interger形式
         int newValue=MyWorker.doubleTheValue(originalValue);//对数字翻倍
         textValue.setText(Integer.toString(newValue));//把新的值赋值到屏幕上

         Snackbar.make(view, "从"+originalValue+"变成"+newValue, Snackbar.LENGTH_LONG)
                 .setAction("Action", null).show();
            }
        });
