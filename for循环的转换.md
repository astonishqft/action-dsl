
## for 循环的定义

#### action dsl

```python
a = [1,3,4]

for b in a:
    message(b)
    for c in a:
        message(c)
    end
end
```

#### 转换的目标json

```json
{
  "type": "message",
  "properties": {
    "title": "message1"
  },
  "childNode": {
    "type": "message",
    "properties": {
      "title": "message2"
    },
    "childNode": {
      "type": "loop",
      "properties": {
        "title": "loop"
      },
      "loopNodes": {
        "type": "message",
        "properties": {
          "title": "message for"
        }
      }
    }
  }
}
```