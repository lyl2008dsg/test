# Diagram Render Test

## 1. Mermaid Flowchart



|      |      |
| ---- | :--: |
|      |      |
|      |      |



2
222222


```java
public class A {
  
}
```
2
```java
sasdfasdf
```
2


[1111.md](1111.md)
```java
public class A {
  aasdf[1.md](1.md)
}
[1111.md](1111.md)
```
<u>222222222</u>
**22222222222**
2
*222222222222*
22
2
```java
123123123
```
2
2
```java
234234
```
2

| 123123123 | 1231 | 123  |
| --------- | ---- | ---- |
|           |      | 123  |
|           | 123  | 123  |
| 123       | 123  |      |



```json
123123

```



```mermaid
flowchart TD
    A([Start]) --> B{Workspace opened?}
    B -- No --> C[Open folder picker]
    C --> D[Load local workspace]
    B -- Yes --> D

    D --> E[User clicks New File]
    E --> F[Create example.md]
    F --> G[Refresh file tree]
    G --> H[Open new file in editor]
    H --> I[Edit Markdown content]
    I --> J{Save?}
    J -- Yes --> K[Write file to disk]
    J -- No --> L[Keep dirty state]
    K --> M([Done])
    L --> I
```

## 2. PlantUML Flowchart

```plantuml
@startuml
title Polarbear Local Markdown Flow

start

:Open Polarbear;

if (Workspace opened?) then (yes)
  :Load file tree;
else (no)
  :Show folder picker;
  :Select local folder;
  :Load workspace;
endif

:Create or open Markdown file;
:Edit content;

if (User presses Save?) then (yes)
  :Write Markdown to disk;
  :Clear dirty state;
else (no)
  :Keep dirty state;
endif

:Render preview;

stop
@enduml
```

## 3. Mermaid Sequence Diagram

```mermaid
sequenceDiagram
    participant U as User
    participant UI as Polarbear UI
    participant T as Tauri Command
    participant FS as Local File System

    U->>UI: Paste screenshot
    UI->>T: save_image_asset(...)
    T->>FS: Write image to assets/
    FS-->>T: Saved
    T-->>UI: ./assets/image-xxx.png
    UI->>UI: Insert Markdown image syntax
    UI->>UI: Refresh Live Preview
```

## 4. PlantUML Sequence Diagram

```plantuml
@startuml
title Paste Screenshot Flow

actor User
participant "Polarbear UI" as UI
participant "Tauri Command" as Tauri
database "Local File System" as FS

User -> UI: Paste screenshot
UI -> Tauri: save_image_asset(...)
Tauri -> FS: Save image to assets/
FS --> Tauri: image path
Tauri --> UI: markdown insert text
UI -> UI: Insert ![image](./assets/xxx.png)
UI -> UI: Refresh Live Preview


@enduml



```



# 5.图片
![image](./assets/image-20260618-215311.png)

2
![image](./assets/image-20260618-215315.png)

2
![image](./assets/image-20260618-215317.png)

22


5. 1
6. 11
7. as
8. d





