---
layout: post
title:  "Design Patterns in Java!"
date:   2026-09-14
categories: software development concepts
---

1. **Creational patterns**
2. **Structural patterns**
3. **Behavioral patterns**

1.1. **Singleton:** To have more control over global instances and also one instance for a class.
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




**References:** refactoring.guru and chatgpt

