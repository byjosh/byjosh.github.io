## Data portability is dire from GUI website makers like Wix and Weebly - but work on filtering pasted HTML has saved it

I read [this Squarespace help article](https://support.squarespace.com/hc/en-us/articles/226312567-Moving-from-Weebly-or-Wix-to-Squarespace) which (in March 2025) says that apart from products one cannot import a Wix or Weebly site to Squarespace.

This lack of portability is looks like lock-in for site platforms (harder for customers to move) - and a product of computer literacy costing time (and the money to have time) in order to learn HTML & CSS. But the platforms (presumably to gain customers) seem to have done work on filtering pasted HTML so that imported styles do not mess up a site - but preserve ability to paste links. And this makes situation a lot better for small websites (half a dozen pages or so).

## The ideal
Ideally HTML contains your content and structure (headings, text, images) and CSS contains the presentation details (what font to use, how big to make the text, colour of text and its alignment etc.). And that separation will usually allow consistent treatment of content - for example: all links are styled the same - unless selected for different styling in the CSS.

## The problem
If one copies text from a website (something with an exotic font is best to demonstrate) and then pastes into a wordprocessor like LibreOffice, or Microsoft Word one can see references to the exotic font in the toolbar when one clicks on the text. By default copying the rich text - including links and formatting - retains a lot of extraneous style information. And historically pasting it into a website editor like Wordpress WYSIWYG editor would preserve that information and result in a messy contrast with the style of the rest of the page (due to mismatch).

## The solution
At the platform level (for Wordpress.com, Wix and Squarespace) it looks like they must be filtering the pasted HTML back to its essentials then integrating it - without style info - into the page it is pasted into. The benefit for them is that new customers don't paste in old site content, see the mismatch, and blame the platform/assume the platform is incompetent. So it likely helps with customer acquistion/retention. Yet for small sites with simple layouts - and in the absence of enough standardisation for true portability - it does help with portability. Because it means one can past text including links and headers and have those structural elements preserved and working - without having to understand the underlying HTML/CSS that is driving the result.

## What the filtering does not solve
The filtering does not solve the issue of complex layouts (which one might not expect to be very portable anyway). And files and images still have to be ported - and references to them updated. But for a lot of content the situation as seen now is a lot better than historically. At an industry level - having standardised HTML for certain features (e.g. image galleries) and mandating large platforms to export in a predictable format would help many customers via allowing other platforms to import that standardised export file.
