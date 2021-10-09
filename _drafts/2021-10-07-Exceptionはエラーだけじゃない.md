#Exception
javaにはというか現在主流のプログラミング言語ではExceptionという仕組みがある。
あらかじめ予測されたトラブルに対してExceptionを定義し、
トラブルを発生させた処理の呼出し元に対応を促す仕組み。
##Exceptionの使い方
###Exceptionの宣言
Exceptionは必要に応じて定義する。
Exceptionを継承したクラスがExceptionとして動作する

    public class ClashException extends Exception {
    }

###トラブルが発生しうる処理側
-処理の宣言部にどんなExceptionが発生するのかを宣言しておく
-トラブルを検知した時点でExceptionを生成してthrowする

    public void run() throws ClashException {
      if (status == 目の前に小石がある) {
    　  throw new ClashException();
      }
      move(spead);
    }
###処理の呼出し側
-呼び出す処理をtryブロックで囲み、発生しうるexceptionに対してのcatchブロックとトラブル対応を記載する

    public void draw() {
       for (People people : peoples) {
         try {
           people.move();
         } catch (小石につまづいたException e) {
           keganinList.add(people);
         }
       }
    }
