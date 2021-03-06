# Working with Education APIs in Microsoft Graph

<!-- This content is not specific to the Education APIs. This overview topic should tell the story about the EDU APIs in Microsoft Graph specifically, rather than the Microsoft Graph API in general (that's covered in other topics).
The Microsoft Graph API provides access to Office 365 resources through one REST endpoint and one access token. This is done by accessing the Graph through a set of URLs like the following examples:

    https://graph.microsost.com/<version>/users
    https://graph.microsost.com/<version>/groups
    https://graph.microsoft.com/<version>/me/calendars
-->

The Education APIs in Microsoft Graph enhance Office 365 resources and data with information that is relevant for education scenarios, including schools, students, teachers, classes, enrollments, and assignments. This makes it easy for you to build solutions that integrate with educational resources.

The Education APIs include two new resources, **Rostering** and [educationAssignment](resources/educationassignment.md), that you can use to interact with the assignment and rostering services in Microsoft Teams. You can use these resources to automate student assignments and manage a school roster.

<!-- What resource should we link to for Rostering? I don't see a Rostering resource topic in the Rostering/resources folder. -->

## Authorization

To call the Education APIs in Microsoft Graph, your app will need the appropriate permissions. 
For more information about permissions for Education APIs, see [Permissions](../../../concepts/permissions_reference.md). 

## Assignments 

You can use the assignment-related Education APIs to integrate with the Assignments service in Microsoft Teams. Microsoft Teams in Office 365 for Education is based on the same Education APIs, and provides a use case for what you can do with the APIs. Your app can use these APIs to interact with assignments throughout the assignment lifecycle. 

<!-- I'm not sure that this text is clear. See the sentence that I added to the previous paragraph; please update to clarify the meaning.
The Public API is the same API that _Microsoft Teams in Office 365 for Education_ built it's user interface with.  Thus, the best sample of what can be built with the Microsoft **Assignments** API is _Microsoft Teams in Office 365 for Education_.  
-->

The following are some common use cases for the assignment-related Education APIs.

|Use case|Description|See also|
|:-------|:----------|:-------|
|Create assignments|An external system can create an assignment for the class and attach resources to the assignment.|[Create assignment](../api/educationassignment_post_resources.md)|
|Read assignment information|An analytics application can get information about assignments and student submissions, including dates and grades.|[Get assignment](../api/educationassignment_get.md)|
|Track student submissions|Your app can provide a teacher dashboard that shows how many submissions from students need to be graded.|[Submission resource](educationsubmission.md)|

## Rostering

The rostering APIs enable you to extract data from a school's Office 365 tenant provisioned with Microsoft School Data Sync. These APIs provide access to information about schools, sections, teachers, students, and rosters. The APIs support both app-only (sync) scenarios, and app + user (interactive) scenarios. The APIs that support interactive scenarios enforce region-appropriate RBAC policies based on the user role calling the API. This provides a consistent API and minimal policy surface, regardless of the administrative configuration within tenants. In addition, the APIs also provide education-specific permissions to ensure that the right user has access to the data.

You can use the rostering APIs to enable an app user to know:

- Who I am
- What classes I attend or teach
- What I need to do and by when

The rostering APIs support support the following scenarios:

- Get roster
- Get schools
- Get classes
- get teachers/students
- Get my schools/classes


## Next steps
Use the Microsoft Graph Education APIs to build education solutions that access student assignments and school rosters. To learn more:

- Explore the resources and methods that are most helpful to your scenario.
- Try the API in the [Graph Explorer](https://developer.microsoft.com/en-us/graph/graph-explorer).

<!-- Verify that we'll have Education API examples in GE? Otherwise, remove the second bullet point. -->

