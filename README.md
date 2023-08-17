# Articles with Images

This repository contains a subset of a Ruby on Rails app. There are 3 models.
`Articles` are a type of `Posting`. Other types of Postings include `Questions` and `ProductReviews`. 
Postings have a `body` attribute. The contents of the Posting is stored as raw html. Some Postings have images embedded within the text of the Posting, in the form of an `<img>` tag wrapped in `<figure>` tags.

The repo also contains one view file and one spec file.

## The Task
Throughout the site, "posting snippets" are displayed, with links to read the full Posting. The product manager has decided that when an Article contains an image, its snippet should display the image above the snippet body. If an Article contains multiple images, only the first image should be displayed.

## Your Task
You are the developer assigned to review the code that was created for this feature. As you review the code, try to answer the following questions:

- Does the implementation achieve the desired effect?
  1. Maybe yes. To do this, you need to run the code and check how it will work. But most likely a trick question.
- What are the shortcomings of this implementation?
- Does the code adhere to best practices?
  1. I wouldn't say so. In the model, we see a lot of logic that shouldn't be there. If we need some kind of logic, we can move it to services or modules in order not to fill the models with unnecessary details. The logic that is described in the model does not specifically belong to it.
- How might you implement this differently?
  1. We can use Nokogiri gem for parsing html (also if we working with site, we need gem open-uri)

#### RSpec
The code includes a unit test, which passes. What is wrong with this unit test? How could it be improved?
- There are small errors in the tests. I would take out part of the logic in the factory, which is responsible for which variables include some text or message or link. Also let I would put under describe.
And in my opinion, the test should not pass, because according to all ROR rules, the directory should be called spec.

### Instructions
Fork this repository. You can either add comments to the existing code explaining what is wrong and/or what you would change and why. Or you can rewrite the feature, highlighting in the comments what was problematic with the original implementation and providing justification for your decisions. Please put a link to your public repository into the answer section of the question.
