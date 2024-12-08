В проекті має бути реалізовано функціонал виведення нумерованого списку імен та імені за певним індексом
за допомогою можливостей Interface List та Class ArrayList. Маємо такий перелік імен:

Alice
Bob
Lucy
Denis
Tom

 Виведення має бути таким:

 Names:
 1) Alice
 2) Bob
 3) Lucy
 4) Denis
 5) Tom

 Name: Lucy is in index 2

(1) Cтворіть проект Names-List на локальній машині через IntelliJ IDEA (IDE).
(2) Структура проекту має бути такою:

(3) Функціонал класу Main

package app;

public class Main {

  public static void main(String[] args) {
    DataRepository repository = new DataRepository();
    DataHandler handler = new DataHandler();
    UIOperator uiOperator = new UIOperator();
    uiOperator.getOutput(handler.formListOutput(repository.getData()));
    uiOperator.getOutput(handler.formOutput(repository.getData(), 2));
  }
}


(4) Функціонал класу UIOperator

package app;

public class UIOperator {

  public void getOutput(String output) {
    System.out.println(output);
  }
}

(5) Доопрацюйте функціонал класу DataRepository

package app;

import java.util.ArrayList;
import java.util.List;

public class DataRepository {
  // Метод повертає список імен
  public List<String> getData() {
    List<String> list = ArrayList<>();

    return list;
  }
}

(6) Доопрацюйте функціонал класу DataHandler

package app;

import java.util.List;
import java.util.concurrent.atomic.AtomicInteger;

public class DataHandler {

  // Метод формує виведення імені за певним індексом
  public String formOutput(List<String> list, int index) {
    try {
      String name = list.
      return "Name: " + name + " is in index " + index;
    } catch (IndexOutOfBoundsException e) {
      return "Wrong index!";
    }
  }

  // Метод формує виведення нумерованого списку імен
  public String formListOutput(List list) {
    StringBuilder sb = new StringBuilder();
    AtomicInteger count = new AtomicInteger(1);
    for (name : ) {
      sb.append(String.("%d) %s%n",
          count.getAndIncrement(), name));
    }
    return "\nNames:\n" + sb;
  }
}

(7) Залийте виконаний проект на свій GitHub репозиторій, посилання на який зазначте в LMS.
