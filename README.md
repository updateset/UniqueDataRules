# UniqueDataRules
Enforce unique data by simulating compound database key via business rules
Use case
ServiceNow inherently has a method to specify a unique value within a table by going to the table configurations and specifying which field should have a unique value. This method is very limiting because it only allows for 1 unique field to be selected within the table and does not allow for more complex database keys to be created such as composite keys, where a combination of values from multiple columns must be unique.

The unique data application allows for these rules to be defined and processed at the business rule level. All while managing everything via a single table view.

Role(s) Required
admin

Fields
Rule Name	Rule Name is used to give the key definition a human readable name.
Active	True | False determine whether to enforce the key definition or not.
Composite Key	True | False this field is used to determine whether each selected field should be treaded as a primary key or a composite key.
Table	The target table to apply the following unique key violation detection rules to.
None Duplicate Fields	The field(s) that need to be unique within the selected table.
Table fields for unique data mappings
Navigation
Navigate to Unique Data -> Unique Data Mappings
Create New

Examples
Example Requirement Simple: Users can only register for an account with their email once. I.E no duplicate emails can be allowed on the user table:


Example Requirement Advance: Groups cannot have the same name if they are in the same hierarchy. I.E I can only allow 1 group named support whose parent is Network.

