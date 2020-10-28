================= Start of Jamil's comments =========================
Task 1:
Code refactoring, understanding and improving.

app/Http/Controllers/Booking.php
In BookingController Coder used Repository Design pattern for example in the index function in controller called the repository function named getUsersJobs($this->repository->getUsersJobs($user_id)) and passed an user id and did main logic in repository function rather then controller.
I changed some code in the index function of BookingController.

Old code 
$response = $this->repository->getUsersJobsHistory( $user_id, $request );

New code
$response = Response::make($contents, $statusCode);
$response->header('Content-Type', $value);
return $response;

we can implement the core logic in the controller for the sake of good understanding of code.
app/Repository/BookingRepository.php
In BookingRepository Coder did all queries which is quite confusing rather than utilize the controller. Queries should be model to keep code simple and readable and effective.
What makes code terrible?
Poor formatting.
Use of no comments to explain the logic.
Compromising on basic structure of Laravel.

================= EOF Jamil's comments =========================

Choose ONE of the following tasks.
Please do not invest more than two hours on this.
Upload your results to a Github Gist, for easier sharing and reviewing.

Thank you and good luck!



Code to refactor
=================
1) app/Http/Controllers/Booking.php
2) app/Repository/BookingRepository.php

Code to write tests
=====================
3) App/Helpers/TeHelper.php method willExpireAt
4) App/Repository/UserRepository.php, method createOrUpdate




What I expect:

A. A readme with:

1.  Your thoughts about the code. What makes it amazing code. Or what makes it ok code. Or what makes it terrible code. How would you have done it. Thoughts on formatting. Logic.. 
2.  Refactor it if you feel it needs formatting. The more love you put into it. The easier for us to asses.  

Make two commits. First commit with original code. Second with your refactor so we can easily trace changes. 

Vänliga hälsningar / Best regards
Virpal Singh
