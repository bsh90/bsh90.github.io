---
layout: post
title:  "Design Patterns in Java!"
date:   2026-09-14
categories: software development concepts
---

1. **Creational patterns**
2. **Structural patterns**
3. **Behavioral patterns**

1.1. **Factory method:** avoid tight coupling between the creator and the concrete products, introduce new or different types of products (Open/closed principle)

One example which the concrete factory is chosen depending on configuration or environment options.
```
public interface Button {
    void render();
}

public class HtmlButton implements Button {
    public void render() {
        System.out.println("Hello World! Html Button");
    }
}

public class WindowsButton implements Button {
    public void render() {
        System.out.println("Hello World! WindowsButton");
    }
}

public abstract class Dialog {
    public void renderWindow() {
        Button okButton = createButton();
        okButton.render()
    }

    public abstract Button createButton();
}

public class HtmlDialog extends Dialog {
    @Override
    public Button createButton() {
        return new HtmlButton();
    }
}
public class WindowsDialog extends Dialog {
    @Override
    public Button createButton() {
        return new WindowsButton();
    }
}

public class Demo {
    private static Dialog dialog;

    public static void main(String[] args) {
        configure();
    }
    static void configure() {
        if (System.getProperty("os.name").equals("Windows 10")) {
            dialog = new WindowsDialog();
        } else {
            dialog = new HtmlDialog();
        }
    }
}
```
second example which the concrete factory is chosen depending on input.
```
interface Notification {
    void send();
}
class EmailNotification implements Notification {
    public void send() {
        System.out.println("Sending email");
    }
}
class SmsNotification implements Notification {
    public void send() {
        System.out.println("Sending SMS");
    }
}
class NotificationFactory {
    public static Notification create(String type) {
        if (type.equalsIgnoreCase("email")) {
            return new EmailNotification();
        }
        if (type.equalsIgnoreCase("sms")) {
            return new SmsNotification();
        }
        throw new IllegalArgumentException("Unknown notification");
    }
}
Notification notification =
        NotificationFactory.create("email");
notification.send();
```

1.4. **Singleton:** To have more control over global instances and also one instance for a class.
```
public final class DatabaseConnection {
    private static DatabaseConnection instance;
    public String value;

    private DatabaseConnection(String value) {
        this.value = value;
    }

    public static DatabaseConnection getInstance(String value) {
        if (instance == null) {
            instance = new DatabaseConnection(value);
        }
        return instance;
    }
}
```


**References:** [refactoring.guru](https://refactoring.guru/design-patterns/catalog) and chatgpt

