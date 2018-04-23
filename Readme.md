# How to view persistent objects in the XtraGrid and edit them in a separate window


<p><strong>Scenario</strong><br />This example demonstrates how to view persistent objects in the <a href="https://documentation.devexpress.com/#windowsforms/clsDevExpressXtraGridGridControltopic">XtraGrid</a> and edit them in a separate window in the scope of <a href="https://documentation.devexpress.com/#XPO/CustomDocument2138">UnitOfWork</a> , so that changes made to the object's properties can be saved or canceled. This approach helps implement a comfortable UI for data input. <br /><img src="https://raw.githubusercontent.com/DevExpress-Examples/how-to-view-persistent-objects-in-the-xtragrid-and-edit-them-in-a-separate-window-e771/7.3.12+/media/4c9fb77b-2799-11e4-80b8-00155d624807.png"><br /><strong>Steps to implement:<br />1. </strong>Add <a href="https://documentation.devexpress.com/#windowsforms/clsDevExpressXtraGridGridControltopic">GridControl</a> to a Form and use <a href="https://documentation.devexpress.com/#XPO/clsDevExpressXpoXPCollectiontopic">XPCollection</a> as a <a href="https://documentation.devexpress.com/#WindowsForms/DevExpressXtraGridGridControl_DataSourcetopic">DataSource</a> as described in the <a href="https://documentation.devexpress.com/#XPO/CustomDocument2260">Tutorial 4 - A Windows Forms Application for Data Editing</a> article.<br /><strong>2. </strong>Add <a href="https://documentation.devexpress.com/#windowsforms/clsDevExpressXtraBarsBarManagertopic">BarManager</a> with 3 <a href="https://documentation.devexpress.com/#windowsforms/clsDevExpressXtraBarsBarButtonItemtopic">BarButtonItems</a> and handle the Click event as shown in the <em>FormViewOrders.xx</em> file. These buttons will be responsible for creation, modification and removing persistent objects. <br /><strong>3</strong>. Add a second Form that will be used for persistent object modifications. This form will use the <a href="https://documentation.devexpress.com/#XPO/CustomDocument2138">UnitOfWork</a> class to work with the passed persistent object. <strong>Unit of Work</strong> keeps tracking every change to every persistent object during transaction that can affect a data store. With a single call of the <a href="https://documentation.devexpress.com/XPO/DevExpressXpoUnitOfWork_CommitChangestopic.aspx">UnitOfWork.CommitChanges</a> method, all the changes made to the persistent objects are automatically saved to a data store.  For implementation details, see <em>FormEditOrder</em>.<br /><br /></p>
<p> </p>
<p><strong>See Also:<br /></strong><a href="https://documentation.devexpress.com/#XPO/CustomDocument2138">Unit of Work</a> <br /><a href="https://www.devexpress.com/Support/Center/p/A2944">XPO Best Practices</a><br /><a href="https://documentation.devexpress.com/#XPO/CustomDocument2020">Connecting to a Data Store</a><br /><a href="https://www.devexpress.com/Support/Center/p/T210787">Editing an XPO object in a separate Form in Server Mode</a><br />A similar approach is used in the demo application shipped with our components and installed to the following directory %Public%\Documents\DevExpress<em> Demos XX.X\Components\WinForms\CS\ContactManagement\ (XX.X is the number of DevExpress components version)<br /></em></p>

<br/>


