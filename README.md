#### Alice in GridResultsPublisher
```java
public class GridResultsPublisher {
  ...
  public void alice(Subscription sub) {

  }
  ...
}
```

#### Exceptional success
```java
Caused by: com.latencybusters.lbm.LBMEOSException: CoreApi-5688-3231: 
TCP server bind (port=20120): (0) The operation completed successfully.
```

#### 12 years of "TODO"
```java
/**
 * Insert the method's description here.
 * Creation date: (4/16/01 3:47:01 PM)
 * @param newHierarchy com.xxxx.xxxxxxxx.reporting.xxxxx.api.datasource.Hierarchy
 */
public void setHierarchy(com.xxxx.xxxxxxxx.reporting.xxxxx.api.datasource.Hierarchy newHierarchy) {
```

#### check if object turned into null
```java
log.debug("allFeeds: " + allFeeds.size()); 
if (allFeeds == null)                      
{                                          
 allFeeds = new ArrayList();               
}
```

#### concrete code
```java
if (userObject instanceof com.xxxx.xxxxxxxx.reporting.xxxxx.api.datasource.Dimension) {
   id = ((com.xxxx.xxxxxxxx.reporting.xxxxx.api.datasource.Dimension) userObject).getID();
	 //System.out.println("Dimension Id: " + id);
}
```

#### definitely not null
```java
if (ds != null) {                                                      
   if (ds != null && ds.getID() != null) {                                                     
      ...
   }
```

#### documented API
```java
/**
 * A convenience method to return "name" attribute.
 * Creation date: (08/06/2002 10:58:32 AM)
 * @return java.lang.String
 */
public String getName();
```

#### documented constructors
```java
/**
 * QueryEngineTest constructor comment.
 */
public QueryEngineTest(...)
```

#### enterprise TDD best practice pattern
```java
@Test
public void testModel()
{
	System.out.println(_topology.toString());
}
```

#### second phase of understanding
```java
boolean secondPhase = false; //this variable is unnecessary but
// aids understanding
if (tempMaster.isStatusOK()) {
  secondPhase = true;
}
else {
  if (tempMasterControl.rollbackTransaction()) {
    // [...]
    throw new IllegalArgumentException("...");
  }
  else {
    log.error("[...]");
    //do master anyway for what else can we do...
    secondPhase = true;
  }
}
if (secondPhase) {
  // [...]
}
```

#### string layout
```java
selectionPanel.add(new JLabel("COB : ", JLabel.RIGHT));
selectionPanel.add(datePicker);
selectionPanel.add(new JLabel("             ", JLabel.RIGHT));
selectionPanel.add(new JLabel("Feed : ", JLabel.RIGHT));
selectionPanel.add(feedCombo);
selectionPanel.add(new JLabel("             ", JLabel.RIGHT));
refreshButton = new JButton("Refresh");
selectionPanel.add(refreshButton);
selectionPanel.add(new JLabel("     ", JLabel.RIGHT));
```

#### true string
```java
id = (Integer) rData.getTagSetID(getSelectedDataSource(),  tags, Boolean.parseBoolean("true"));
```

#### waiting sleeping beauty
```java
// while Refresh is in progress, donot return to the caller, wait until the
// refresh finishes, so that user will surely no there is no refresh
// Sleep thread for 1 second
try
{
	//	Thread.currentThread().sleep(5000);
	Thread.currentThread().wait(5000);
}
catch (Exception e)
{
	log.info("Error during sleeping thread for 5 seconds before checking isRefreshInProgress : ");
	blockRefData = oldBlockRefData;
	e.printStackTrace();
	throw new XxxxxException("Error during sleeping thread for 5 seconds before checking isRefreshInProgress : ");
}
```

#### yield UI
```java
protected void initGUI() {
	Thread.yield();
 
	controller = new FeedMenuBar();
	FeedInfoPanel infoPanel = new FeedInfoPanel();
	SlaInfoPanel slaInfoPanel = new SlaInfoPanel();
	Thread.yield();
	FeedMappingPanel mappingPanel = new FeedMappingPanel();
	FeedUserPanel userPanel = new FeedUserPanel();
	...
}
```

#### etard test
```java
public class CodingTest {
  @Test
  public void encodingWorks() {
    String payload = "a\t\n\retard\nvalue";
    String encoded = Coding.encode(payload);
    Assert.assertEquals("a_~t__~n__~r_etard_~n_value", encoded);
    ...
  }
}
```
