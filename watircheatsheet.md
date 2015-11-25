
<h1>Watir Cheat Sheet</h1>

<h3>Setup</h3>
<p>browser = Watir::Browser.new</p>

<h4>Navigate to webpage</h4>
<p>browser.goto <em>Enter email address here!</em></p>

<h3>Checking Commands</h3>
<p>browser.status</p>
<p>browser.text</p>
<p>browser.text.include? "Hello"</p>
<p>browser.p</p>
<p>browser.a</p>
<p>element.flash - flashes the element<br/>
element.class - class of the element<br/>
element.exists?<br/>
element.visible?<br/>
element.present?<br/>
element.readonly?<br/>
element.disabled?<br/>
element.enabled?</p>

<h3>Input Commands</h3>
<p>browser.input <br/>
browser.text_field<br/>
browser.text_field name: "name" - with<br/>
browser.text_field name: /name/ - with regex<br/>
browser.lis id: /^foo.*/<br/>
element.set "Hello" - puts hello into the text field <br/>
element.value - returns the value "Hello" <br/>
element.id - returns the set id for the element <br/>
element.name - returns the name for the element<br/>
element.attribute_value "name" <br/>
element.click <em>if clickable</em><br/>

Checking the elements for a text field (some of them work on other things)
</p>

<h3>Table Commands</h3>
<p>table = browsser.table<br/>
table[0] - returns the first table row.<br/>
table[0][0] - returns the first table row table cell<br/>
table[0][0].text - returns the text within it</p>

<h3>Implicit Wait Commands</h3>
<p>browser.driver.manage.timeouts.implicit_wait= 3<br/>
  -sets implicit wait to 3 seconds<br/>
browser.text_field(id: "entry_1000000").wait_until_present<br/>
browser.text_field(id: "entry_1000000").when_present.set "foo" </p>
<p>
Watir::Wait.until do <br/>
  browser.text.include? "Thank you"<br/>
end
</p>

