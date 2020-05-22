# Members
Members model has multiple relationships & business logic around it. Which makes for a lot of code duplications. In-order to mitigate this issue, We'll use DRY  "Don't Repeat Yourself" principle to abstract away some functionality.

Inside `app/Actions/MemberRelationshipsSync` trait, Will allow us the liberty to duplicate member association logic.

Our `Models/Member` model will make use of this trait.