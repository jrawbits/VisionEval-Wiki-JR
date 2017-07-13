For my Personal Experience case study from Intel WiDi receiver open source project - our team developed open source software that anyone could “license” for their own products. The software was called “WiDi” and used the “Miracast” standard. 

We charged a nominal $200 fee for “overhead” IF you wanted to use our “Intel Inside” logo on your product
Then you had to pay $200 and go through our certification process (a student ran some tests), if not – then no charge. 

Here’s how the process worked…

1. Library Manager or Czar did version control, maintained test abd dev environment, checked-in code from submittals etc. Several of us backed him up and had access to his IDE in case he was on vacation etc.
2. Release Manager received submittal modules from the public (mostly OEM’s like Samsung, Lenovo etc.) – scanned them with our scanning tools to ensure malware wasn’t present and ran them in our test/dev environment with our latest version. We had a student intern run a scope/template of tests against each version release. Did it work? If yes –then Passed to Library Manager/Czar to include in Next release; If no, then send back to submitter with explanation of bugs.
3. New versions of code were released on our website Every Other Friday – which included all the “Passed” submissions we had received. When our library manager was ready for the release to be published – he would check-in the new code with Jenkins, we would package it up with our SDK package and place it on our external Website for release along with Release Notes about what features have been added etc.

Generally we used an AGILE type process but it was very loosely applied – no official scrum masters and all that jazz.

In terms of governance – that was largely the responsibility of our Product Manager who approved/disapproved any feature functionality etc in version release meetings weekly.

All in all – the RELEASE side of this open software project required about 5 FTE’s – Product Manager, Library Manager, Release Manager, Student Tester, and a Sales engineer.

