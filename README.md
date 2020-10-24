## Welcome to my GitHub profile <visitor>

```javacript
onVisitorEntered(evt) {
  let visitorName = evt && evt.visitor ? evt.visitor : '<visitor>'
  this.setTitle(`Welcome to my GitHub profile ${visitorName}`;

  this.backendService.logVisitorPromise(visitorName)
                     .catch(error => console.error('Could not log visitor:', error)); 
}
```

```C#
public LogVisitorResponse LogVisitor(LogVisitorEvent evt) 
{
  try
  {
    m_Logger.Instance.LogVisitor(evt.Name);
  }
  catch (Exception ex)
  {
    return new LogVisitorResponse("An error occured :(");
  }
}
```
