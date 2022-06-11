## Welcome to my GitHub profile !

```javascript
onVisitorEntered(evt) {
  let visitorName = evt && evt.visitor ? evt.visitor : '';
  this.setTitle(`Welcome to my GitHub profile ${visitorName}!`;

  this.backendService.logVisitorPromise(visitorName)
                     .catch(error => console.error('Could not log visitor:', error)); 
}
```

```C#
public LogVisitorResponse LogVisitor(LogVisitorEvent evt) 
{
  try
  {
    _logger.Instance.LogVisitor(evt.Name);
  }
  catch (Exception ex)
  {
    return new LogVisitorResponse("An unexpected error occured :(");
  }
}
```
