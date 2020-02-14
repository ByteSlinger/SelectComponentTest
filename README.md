# SelectComponentTest
 Blazor Component that uses a select list that updates the parent

There are many Blazor Component examples out there.  But I couldn't find one that uses a select/option list.

I quickly copied an input text field example component and replaced it with a select/option list.  But following the Microsoft examples, it required a button to trigger passing the selected option back to the parent variable.  I needed a component with a select dropdown that automatically updates the parent when the user selects an option.

The trick was to have a custom setter on the bind string variable that calls InvokeAsync() on the xxxxChanged class.  Look at the SelectComponent.pages source to see the code:

  [Pages/SelectComponent.razor](./Pages/SelectComponent.razor)
