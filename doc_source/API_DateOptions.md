# DateOptions<a name="API_DateOptions"></a>

## Description<a name="API_DateOptions_Description"></a>

Options for a date field\. Dates and times are specified in UTC \(Coordinated Universal Time\) according to IETF RFC3339: yyyy\-mm\-ddT00:00:00Z\. Present if `IndexFieldType` specifies the field is of type `date`\. All options are enabled by default\.

## Contents<a name="API_DateOptions_Contents"></a>

 **DefaultValue**   
 A value to use for the field if the field isn't specified for a document\.   
Type: String  
 Length constraints: Minimum length of 0\. Maximum length of 1024\.   
 Required: No 

 **FacetEnabled**   
Whether facet information can be returned for the field\.  
Type: Boolean  
 Required: No 

 **ReturnEnabled**   
Whether the contents of the field can be returned in the search results\.  
Type: Boolean  
 Required: No 

 **SearchEnabled**   
Whether the contents of the field are searchable\.  
Type: Boolean  
 Required: No 

 **SortEnabled**   
Whether the field can be used to sort the search results\.  
Type: Boolean  
 Required: No 

 **SourceField**   
A string that represents the name of an index field\. CloudSearch supports regular index fields as well as dynamic fields\. A dynamic field's name defines a pattern that begins or ends with a wildcard\. Any document fields that don't map to a regular index field but do match a dynamic field's pattern are configured with the dynamic field's indexing options\.   
Regular field names begin with a letter and can contain the following characters: a\-z \(lowercase\), 0\-9, and \_ \(underscore\)\. Dynamic field names must begin or end with a wildcard \(\*\)\. The wildcard can also be the only character in a dynamic field name\. Multiple wildcards, and wildcards embedded within a string are not supported\.   
The name `score` is reserved and cannot be used as a field name\. To reference a document's ID, you can use the name `_id`\.   
Type: String  
 Length constraints: Minimum length of 1\. Maximum length of 64\.   
 Required: No 