# Basic article parsing exercise

This is version _0.2.0_. All changes beyond grammar will result in an increment. Higher level increments reflect larger changes that may reflect new ways of doing things, or differences in user interfaces, etc.

_You can ask for help and clarification live in person on [Gitter](https://gitter.im/SpeciesFileGroup/taxonworks)!_

## Overview

In TaxonWorks there may be different ways to accomplish the same thing. Nevertheless as it develops and matures some workflows will converge. This manual is a walk through of what might be done when parsing through a single, simple, paper. Its goal is to get you familiar with basics, with hints on how to become a more efficient user along the way. This workflow may not be optimal for much larger papers, though its approach is becoming increasingly effective.

## Exercise target audience

This exercise was originally written with the curators of the John Noyes Universal Chalcidoidea Database in mind. Your ultimate workflow depends on the curators and their priorities.

## Exercise goals

The goals are to describe:

* the basic manual approach to a relatively in-depth curation of data from a single publication into TaxonWorks
* how to capture _all_ aspects of nomenclature recorded in the publication
* how to capture the basic distribution data (citation based) in that paper
* how to capture the biological relationships described in the paper
* how to capture the various topics the paper covers with respect to the taxa in it
* how to capture common names

At the end of the exercise you should:

* be able to add a name to the nomenclature with a significant levels of detail
* review the addition in a catalog view format
* review additions in the context of source
* use a radial annotator to add a biological association
* use a radial annotator to add an asserted distibution
* use a radial annotator to add citation topics
* use a radial annotator to add common names
* be familiar with a number of the commonly used icons (`Radial annotator`, `OTU radial`, `OTU navigator`)

In addition there is help here in the `Addendum` on how to configure various baseline project data, for example `biological relationships` (things like "parasitoid / host"), `topics` (like "Biological control" in the context of a paper and taxon), `biocuration classes` (things like sex, lifestage, etc.).

## Assumptions

* _Various steps here assume you are using a Species File Group sandbox instances that are populated with source, and nomenclature data derived from the Universal Chalcidoidea database. If you are not sure whether this is the case we suggest reading through the whole exercise to get a general understanding of the process, then seeing if you can adapt yourself through the exercise as needed._
* It is often more efficient to do one thing at a time for a set of data. Here we break this rule various times, for example we may want to gather 40 references and then just capture the reference data, then move to capturing one aspect of the data for each paper, then move to the next aspect. We might also be able to take advantage of bulk processing or other services. Again this exercise ignores these paths.
* We assume the reader knows that the circular icons on the right of the screen are slideouts, and they know the name of each slideout (but not necessarily how they are used).
* We assume the reader is familiar with the mechanism to favourite tasks and data cards in the TaxonWorks hub.
* We assume the read is familiar with navigating to a Data card.
* We assume you have the following cards on your hub Favorites tab:
 - *Tasks*
  - Browse nomenclature
  - New taxon name
  - New source
  - Filter sources
  - Source hub (includes links to "New source" and "Filter sources")
  - Manage controlled vocabulary terms

## Gotchas

* Someone might have done the exercise in your sandbox project already! If so we recommend pretending that the they haven't, and simply append or change letters to the taxon names, or other values in question.
* If you don't have corresponding data already in the project various searches and steps may not be triggered.
* TaxonWorks is only officially supported on Firefox and Chrome.
* _As a technical note this was written for TaxonWorks post commit [1a36d3b](https://github.com/SpeciesFileGroup/taxonworks/tree/1a36d3b)._

## Tips

* Use tab to navigate between fields, and onto buttons
* Use enter, while on a button, to click it
* Learn the hotkeys! See the `orange help icon`. The keys there will change in context with the page being clicked on.

## Related exercises

_None._

## Exercise

### Syntax

- In the exercise bulleted points are actions you should take, non-bulleted tasks are comments or guiding questions.
- `Highlighted words` refer to text or elements in the application, for example button or field names.
- "Quoted words" are literal values to be input or noticed

### Capture the source

The source (reference) for this exercise is http://dx.doi.org/10.11646/zootaxa.4521.2.6.

* Find the source in your web-browser, we recommend you keep page open for cross referencing.
* Download the pdf, remember where you put it.

You may not need to download the pdf in general if you get familiar with checking for the source first (see below).

#### Check to see if the source exists

_If at any step you do not find your source, skip ahead to `Adding a new Source` then come back here and continue on if you wish._

* Navigate to the `Source hub` task
* Click the `Find sources` button
* Enter "Hayat 2018", click `Find`
* In the result table click on the Year tab to sort from earliest to latest year.
* Try "Hayat" by itself. Repeat the year sort. How is it different?
* Try a keyword from the title, choose something that would be relatively unique, like "Karnataka". Try again with the year: "Karnataka 2018".
* What happens to the search results when a year is added to the query?
* What about a year with a letter (e.g. "1947a")?

#### Ensure the source is in your project

Sources are shared across all projects, but a set of sources can be tracked per project.

* If the source is added to the project then the row containing our source in the result table should have a `Red arrow/folder icon` that lets you remove that source from the project.
 * If your source is used in citations within the project then you will be prevented from removing it from the project.
* If the `Arrow/folder icon` is green then clicking it will add the source to the project.

#### Pin the found Source
_This assumes you completed the search above._

* Pin the source to you pinboard by clicking the corresponding green `Pin` icon in the result row (or top right of the show screen if coming from the instructions below). It will turn red if is on your pinboard (click again to remove, and set the state to green).

In general a green button means something is persisted in the database (in this case the fact that you have added something to your pinboard), a red button means something is removed from the database (in this case you would remove the flag that says "put this in my pinboard"). Red and green rules hold throughout TaxonWorks.

* Confirm that the Source is now on your pinboard by clicking the `Pinboard` slideout on the right (Green circle with white pin)
* Make the source in your pinboard your default source- with the Pinboard open hover over the "hamburger" menu (three horizontal lines).
* Click the green circle that pops up, the icon turns red and the menu quickly closes
* Hover over the menu to double check that the circle check mark is red.

Only one record of a given type on the binboard can be defaulted to at a time, clicking a second record moves the red check to that record.

#### Attaching a pdf
_This assumes you completed the search above and are in the `Find sources`, although you can attach and do similar checks anywhere the radial annotator for the source is present._

* If you are tracking Pdfs (this is a private research project, pdfs are not shared outside your research) then check to see if a Pdf is loaded by looking for the `Pdf` link in the `Documents` column.

If there is no Pdf link you can add it to the Pdf. This functionality is available anywhere you see the Source and its associated Radial annotator.

* In `Find sources` you can see the annotator (blue circle with caterpillar-like white pie sections) under the `Annotate` column.
* Click the corresponding Radial annotator icon.
* Click `Documentation`
* Position your browser so that you can see your filesystem in one window, and the browser window with the open form in another
* Click on your pdf, and drag it to the box that says `Drop documents here`

Your pdf will automatically load. A successfull load is confirmed with a row below the window that re-lists the citation of the source. It has a red trash can beside it. Clicking the trash can will prompt you to destroy the *pdf* (not the source).
* Close the annotator window by clicking on the gray `x` (top right) or anywhere towards the margins of your screen.
* Open the `Pinboard` slide-out
* Mouse over the hamburger menu
* Click the blue 'Pdf' icon, the pdf viewer will slide out to show the pdf
* Click the edge of the Pdf window to drag the window smaller or larger
* Click the Pdf icon in the middle to close the window

A note about the in-application viewer (short version- beware, don't expect it to be too good). Pdfs are extremely non-standard messes. This is a viewer from a JavaScript library, it will not work well for many pdfs. You are likely better off *not* depending on it. We have some nice integrations that work, sort of (e.g. clicking to navigating to a page, automatically citing the pdf when content is copied from it), but those are yet undocumented and highly experimental.

#### Adding a new Source

If the source does not exist in the steps above it will need to be added. There are several ways to add sources, some of them semi-automated. Here we use a query to CrossRef to use a semi-automated approach.

* Open the `New source` task. You can also access it through the `Source hub` task.
* Click the blue `CrossRef` button
* Paste the DOI: "http://dx.doi.org/10.11646/zootaxa.4521.2.6"
* Click `Find`
* Confirm that the parsed result in the New source form is the source you are looking for. This is important, Crossref will almost always find a hit, however it may not be correct.
* This is now a good point at which to check the values in the form to edit any that may be incorrect, or to add values that are missing. For example CrossRef results may not have pages.

<strike> Functionality currently moved/absent and likely returned in another fashion:
* Check the box `Also create people from authors and editors of BibTeX source?`
This parses out the authors into People records while it adds the source. Note that this will result in duplicate people. There is a utility to merge people that can be used from time to time.
* Note: In practice some find the more efficient way is to not parse authors but rather add People manually. This will avoid duplication and possible cleaning steps in the database.
</strike>

* Click `Save` or more efficiently `Ctrl-s/Alt-s` (function key varies across operating systems) to save the source.
* Notice the source as it would be seen in a citation section is now listed on the top where once there was the text "New record"
* Creating a source automatically adds it to your project.
* Notice the `Red arrow/folder icon` this allows you to remove the source from the project. It does not destroy the source itself.
* Click the `Green pin icon` to pin your source to the pinboard.

* Alternatively follow the steps for `Pin the found Source` and `Attaching a pdf` above

##### On Authors
* Author strings coming from CrossRef are taken verbatim and stored in `Author(s)`
* You may want to assign (creating as needed) People as authors at this point.
* Linking People to a source at this time is a best practice, but it may not be the most efficient practice.
* After selecting a person you may navigate to them in a new tab by clicking on their linked name.
* A task `Uniquify people` exists to de-duplicate (merge) people.

##### On Serials
* Like the `Author(s)`/Person relationship there is a `Journal`/Serial relationship.
* Serials are repeated publications, most will know these as Journals.
* TaxonWorks has a shared, curated Serial list accessible through data cards.
* Assign a Serial by using the `Serial` [smart-selector](SMART_SELECTOR.md).
* If you assign a Serial to a Source then it will take the title of that Serial as the `Journal` value when it renders the citation.

_Aside_: At this point you may want to step through and capture other sources in the References cited section for future reference. This might be particularly important if you are adding names that are synonyms of prior work.

### Capture the nomenclature

Before starting page through the publication. Get a feel for how many names, host records, and distribution data there are. Get a feel for what is new to this publication, versus what is being re-cited. It might be useful to create a checklist of the names that will be checked prior to going through the paper, or it can be done as you go, here we note we'll have to track following nomenclature (a partial list):

1. Encyrtinae, Encyrtidae
2. The new species _Ooencyrtus xenasteiae_ Hayat & Gupta
3. The (host) family Xenasteiidae
4. The host genus _Xenasteia_
5. A un-named taxon "_Xenasteia_ sp."
6. A common name "rugose spiralling whitefly"
7. A host for the common name _Aleurodicus rugioperculatus_ Martin (Hemiptera: Aleyrodidae)
... etc.

#### Start with the target taxa

In this case the wasps are the group being curated, they are the target taxa.

TaxonWorks nomenclature is based on monomials, i.e. each single word element has its own record. Behind the scenes the database links these single monomials ("Protonyms") together to represent the various name-strings as we are used to seeing them. A "Combination" in TaxonWorks is in fact also another single record, one that has no value in its name field. Within Combinatoins the name-string a user sees is built up by relating Protonyms to this "anonymous" Combination record. For example the combination "Aus bus (Smith, 1920)" consists of three TaxonName records: 1) the Combination record (with nothing in its name field), and 2-3) two other protonyms "Aus" and "bus". The two protonyms are related to the Combination with specific records indicating how they are being used (e.g. as a species, as a genus). All of this is hidden from the user in the user interfaces, but it can be important to understand the underlying model when representing complicated nomenclatural histories.

Given this we need a strategy for composing our names.

The basic, manual approach (there are others) is:

1. Search for the protonym in question
2. Add it if it doesn't exist
3. Repeat

In practice the search step happens many times at once by using the `Browse nomenclature` task. The addition is sped up by a number of nice macro tricks as well, so the loop is actually quite efficient.

#### Searching for a taxon name

There are two basic ways of going about this:

* Go to the `Browse Nomenclature` task.
* Using the navigation section on the left either navigate to the family `Encyrtinae` via clicking through the hierarchy or search for it using the `Search field`.
* Use the `New taxon name` task to search while adding a new name. When you enter a monomial value into the name field it will automatically search to see if there are matches in the system.
* Start with "Encyrtidae", does it exist?
* Repeat this down to "Ooencyrtus"
* Use both approaches documented above to search

#### Adding a name

Let's assume the name `Ooencyrtus` does not exist and add it.

* Open the `New taxon name` task

_Tip: The `orange slidout help icon` on this task is particularly useful._

* Enter "Ooencyrtus" into `Name`
* Choose the parent for the name by typing and selecting a row from Parent. You might use the subfamily, but if you're starting in a new project you could do something like attach it to "Root"
* If you are adding a child to "Root" you must then assign its nomenclatural code, all other times the code is inferred from the parent rank.

Note that you can add any name to any higher rank! Each project has a "Root" name at the very top (bottom?).

* Choose the rank of `genus`

The rank prediction is smart, and gives you the most likely rank for the name given the parent's rank.

* If you do not see the rank you are looking for click `show all`
* Click `Create`, or, more efficiently, click `Ctrl-s/Alt-s` to save your record

Note that keybindings may differ in Windows, see the `Orange help slideout` on the ride side of the screen for more.

Notice that the name `Ooencyrtus` appears in the column to the right at the top; this is what the name will look like when rendered (in most cases). Besides the name is the `Radial annotator` which can be used to add annotations.

* Add the authorship to the name. In the Author section click `Verbatim` and type "Ashmead". Save the record, note the author name appears beside the name.

_In the UCD you will note that the literature exists for that record, if so you can search for and find it in the Source tab._

* Pin "Ooencyrtus" to the pinboard using the green `Pin` button beside the name on the upper right display window, the round pinned icon should turn red.
* Open the pinboard and set "Ooencyrtus" as the default taxon name using the `Check icon` under the `hamburger menu` (see Sources above).
* Pinning in this manner lets us quickly related the pinned record to new records.

Add the new species.

_Advanced trick._ With the `Edit taxon name` page open and a record saved you can type `Ctrl-d/Alt-d` to pass the current name in to a new form as the parent of a new name! That is, `Ctrl-d/Alt-d` opens a new name form so you can create a child of the current name.

* Use the advanced trick, or click `New` in the `New taxon name task` or use `Ctrl-n/Alt-n` to open a new (empty) form
* Type "xenasteiae"
* Click the blue `Pin icon` to apply the pinned "Ooencyrtus" as the Parent
* Notice the rank is already predicted and set to species

* Click `Create` or type `Ctrl-s/Alt-s` to save the record

Time to assign authorship. We can automatically assign authorship of the species to the authors of our source.

* Select the `Source` tab in `Author`
* Click the blue `Pin icon` to assign the pinned source
* In the citation line fill in the `Pages` input with the page number- "259"

The `Pages` input is free text, including ranges, etc. You'll want to fill it consistently according to your team/project's goals.

* What happens to the authorship string beside the name as rendered in the top right?

Wait, in the paper, only two of the source's authors are listed as authors, let's fix that!

* Click the `Person` button under `Author`. Type "Hayat'. Select the record from the list

Note that there may be other Hayat records in People. People can be merged at future times. When you are selecting a person note their active/life period and the number of times that record has been used, this can help you differentiate between people. When people are assigned to roles (e.g. taxon name authors) that have years in the related data, then their active/life years are automatically updated. Those values can also be manually edited by navigating to person from corresponding Data card.

* Add the other taxon name author, "Gupta".
* Click and hold on the right of row with "Gupta" and drag the row up, release the name. Authors can be re-ordered in this fashion.
* Return the author order to the correct order

Now document the original combination for the species.

* Scroll down to `Original combination and classification` section.
* Click `Set as current`. The genus and species inputs are filled automatically based on the current parenthood of this name.

Alternatively, to see the original combination you can drag the species name down to its original placement.

* Click the `red trash can` beside the rendered name at the bottom to clear the original combination added above.
* Click the arrows and drag it down to the species slot, release it.
* Note that "[GENUS NOT SPECIFIED]" is listed when no genus is provided.
* Click into the `Genus input`, search for "Ooencyrtus" and select it. Note the name is automatically updated.
* Move to the `Gender and form` section.
* Assign the form, it should be __TODO: Taxonomists, what should the values be?!__.

Update the etymology.

* Copy the etymology from the paper - "The species name is derived from the generic name of the host insect, Xenasteia."
* Paste it into the `Etymology` text area.
* The text area accepts Markdown, you can italicize "Xenastei" by adding underscores to either side: `_Xenasteia_`. Do this by typing or highlighting your text and clicking the `I formatting icon` on the icon bar.
* Click the `eye icon` (right of the icon bar) to preview the text appearance. Toggle back to edit with the same button.

Select part of speech.

* This is particulary useful for the future, when the species is moved from one genus to another
* if the name is adjective, 3 alternative forms for each gender is assigned to the name. Those forms could be edited.

#### Assign type material

Time to assign the type material. Our goal here is to capture the provided information verbatim. If at a later time we need to break down this information we can reference the PDF and the recorded data.

* In the `Type` section click on `Quick`. Note that you are taken to a new browser tab. You can use your browsers hot-keys to navigate between tabs.
* Add the holotype- click the `radio-button beside Holotype`
* Copy the verbatim label information from the Pdf, editing it to remove quotes so it looks like:

```
INDIA: KARNATAKA: Udupi, Malpe beach, 1.v.2017, Coll. K. Selvaraj

Ex. Pupa of Xenasteia sp. on Calophyllum inophyllum L.
```

* Paste it in the `Buffered collecting event` field

"Buffered" data are fields that stay with the collection object record, in this case we mean "area used to store data temporarily". Later these data can be broken down into collecting events or determinations. Buffered data fields are not intended to be subsequently edited, in this way they are write-once, read many.

* Click the `Create` button

Notice the `right column` is now updated. There, summarized in the top most box is the target taxon name along with a brief record of the specimen in question. There is a radial annotator that is available to annotate this specific Type Material assignment. Below the record summary is a `list of all type material` for that name. The currently selected type material record is the `row in green`. The green row determines the corresponding collection object that is visible to the left `Collection object` section.

#### Advanced type material attributes

At this point there are several additional attributes for our specimen that can be discussed.

Let's add the catalog number "No. ICAR/NBAIR/1517 A" to the holotype specimen. In TaxonWorks "Local" identifiers (i.e. identifier schemes that are designed without significant effort to ensure their global uniqueness) have two components: a namespace (part of the unique string that stay the same for all members of the set of things that bear this type of identifiers) in this case "ICAR/NBAIR/" and an identifier (part of the unique string that changes from member to member), in this case "1517 A".

With a well written paper it is straightforward to synchronize TaxonWorks with the namespaces being used by referencing the materials and methods section for the repository (depository in some) section. There can be problems here however, for example in this paper one repository acronym is missing (HYM.CH), and another is not the same as what is listed (NBAIR != "ICAR/NBAIR/").

Note that namespaces are shared across projects, so just because you, or other curators in this project haven't added the namespace doesn't mean it is not there.

* Navigate to the `Namespaces` card on the Data tab.

_Aside_: You can leave the type material form open and open the hub in a new tab, then access the `Namespace card` from there. Opening a new tab is typically Ctrl-click of a link (or as per your OS/browser). Note that every time you land on a new hub tab your cursor is placed in input of the filter box. This means you can start typing ("Names...") to immediately narrow down the card on the page. A power user will then tab to the card, move between the cards with arrows, and select the task or data card without using their hands leaving the keyboard.

* Search for "NBAIR" in the `Namespace search field`, if not found click the `New button` beside it
* Note that per the Materials and methods section the `Institution` is "ICAR-National Bureau of Agricultural Insect Resources, Bengaluru, India", fill in the field
* Also use this value for the `Full name` field, as we know no other formal name.
* Use "ICAR/NBAIR/" for the short name (it's what we see in the actual material examined section, though you may choose to ignore this fact and use "NBAIR" as listed in the materials and methods)

Leave the `Verbatim short name` empty, we use it only when there is a uniqueness conflict with short name. TaxonWorks "encourages" users to think hard before minting a `short name` namespace that may be exposed in many places.

* Click `Create Namespace`
* Use the `New button` on the `left column` to repeat this process for "ZDAMU" and "HYM.CH." (you'll have to decipher the institute for the latter, some of you likely know).
* If you need to, return to the browser tab with the `Edit type specimen` form.

_Aside_: You can use (Shift)-Ctrl "{" or "}" to move back or forth between browser tabs in Firefox.

* Double check that you are editing the `holotype row` (green highlighted row on upper right corner)
* In the `Identifier` section search for "ICA" in the `Namespace smart selector search tab`, select the appropriate row.
* Fill in "1517 A" in `identifier`

Assign the sex to the specimen:

If you wish to record the verbatim label indicating sex use `Buffered determinations`
* Enter "Female" in `Buffered determinations`

Specific attributes like sex or stage assigned to collection objects during the course of their curation are called "Biocuration classes" in TaxonWorks. These are managed in the `Manage biocuration classes and groups` task. If the project has set these attributes you will see `green buttons` below the `Collecting event input` *after* the record has been created (in this form), if you do not then see the "Managing biocuration classes and groups" in Addendum below.

* Click on the `green "Female" button`, it will turn red, meaning that you have written the attribute to the record.
* Click the red button again to destroy the attribute, removing it.

Green, create, red, destroy.

* The `Preparation type` can be selected from the list

If the preparation type is not listed it can be added (once) using the `Preparations card` from the `Data cards tab`. Typically administrators will set this list for you prior to entering data. Preparation types are shared between projects, ultimately they will become a controlled vocabulary.

* The `Repository` can be selected from a controlled vocabulary list. Th present list is derived primarily from the now defunct [grpbio website](http://grbio.org).
* If you can not find the repository add it via the `Repository data card` (open the hub in a new tab), then return to this form.

* The `Collecting event` selector is not useful in this context unless you decide to turn the verbatim label data into a collecting event, but that's another tutorial.

You can add advanced properties to your specimen via the `Expanded edit` link. This will open in a new tab.

Add the paratypes.

Unfortunately the manuscript is very unclear as to what is going on here. The count states 4 female, 3 male, then goes on to list 2,2, 2,2, and 2,1 specimens (female, male respectively). This doesn't add up, so perhaps not all specimens are paratypes? The paper also lists 2 slides with 3 numbers namespaced "EH" (which isn't referenced anywhere), so it is unclear if the specimens are numbered individually on the slides, or what is going on here. We're going to solve this by creating one record, and dumping the verbatim paratype data in there from the paper, noting as such.

* Click the `blue "New type" button` on the right column
* Click `"paratype" in the radio button`
* In the `Total`, type 7.
* Click `Create`

* Click the `radial annotator`.
* Click `Notes`
* Paste in "Paratype information is difficult to decipher, here is the verbatim information: "Paratypes: 4 ♀, 3 ♂ (2 ♀ and 2 ♂ on 3 slides, Nos EH.2336, EH.2337, EH.2338), with data same as for holotype. (2 ♀ and 2 ♂, on 3 slides, in ZDAMU; registration No. HYM.CH.798; 2 ♀, 1 ♂, in NBAIR; registration Nos ICAR/NBAIR/1517 B)."
* Click `Create`
* Click `X` to leave the annotator.

•	Go to “Manage biocuration classes and groups” in the Addendum below. Complete the exercise then return here.

* Click `Male` and `Female` in the `Biocurations' section` (you may have to reload the page to see the buttons).

_Aside_: Note the biocuration buttons are Green and Red. A reminder that in TaxonWorks these colors mean they will alter data directly in the database, without the need for further update/save clicks.

Let's check out what we have thus far:

* Click on the name `Ooencyrtus xenasteiae HAYAT & GUPTA, 2018` on the top right of the type material form, you are taken to the `Browse nomenclature` section.
* Check the soft validation warnings on the right, are there any? Soft validation messages are there to indicate ways in which the data can be improved, or are in conflict.

_If you see something incorrect you can quickly toggle to the Edit page using `Ctrl-t/Alt-t`_

##### Adding non-target names

In some cases we don't need to add non-target nomenclature to set ourselves up for capturing host/parasite data, but here the data is straightforward. We don't need the level of detail we have for our target group, we just need a hierarchy we can tie to our OTUs.

Add the following names as needed. When you create "Plantae" assign it to Root as parent, and choose the correct nomenclatural code when prompted (ICN). For authorship use the `Verbatim" field`, or select/create a new person. This can be done inline in the `Person` tab after searching.

_This should take 2 minutes or less. Remember your hotkeys, you should never(?) need to touch the mouse once you start. `Ctrl-s/Alt-s` (save record), `Ctrl-n/Atl-n` (new record), `Ctrl-d/Alt-d` (new child)._

```
Root
 Animalia
  Diptera
   Xenasteiidae
    Xenasteia
  Hemiptera
   Aleyrodidae
    Aleurodicus
     rugioperculatus Martin
 Plantae
  Calophyllaceae
    Calophyllum
     inophyllum L.
```

### Biological information

We've more or less completed the nomenclature at this step. We add biological information to taxa (OTUs in TaxonWorks), these OTUs are created on the fly as needed based off the nomenclature.

* In the `Browse nomenclature` task navigate via search or hierarchy on the left to our target species "xenasteiae"

Note that the `OTU navigator` button (closed hexagon with left pointing arrow), top right, is green. This means no OTU exists for the name yet. Clicking it creates the OTU, and takes you to the taxon page. Ulimately you'll see a complete summary on that taxon page. The `OTU radial button` is the dashed hexagon. It does the same thing- creating an OTU if needed, then it takes you to options for adding data to the OTU.

* Click the `OTU radial` (dashed hexagon)
* Click the `X` to close the modal window (a modal window is one that requires an action to close before you can get back to the main page)

Note that both `OTU buttons are now blue`. The button is blue since clicking it is now just an action, the underlying OTU has been created.

#### Tagging the citation with topics

The Universal Chalcidoidea Database (UCD) includes many (134!) different annotations used to indicate that a particular Topic is present on this taxon for a given source. For example these include "Pathogens", "Reproduction", "Revision", "Sampling", Parasitism" and many more. _Your project might not have these tags._

* See the Addendum "Adding Topics" to ensure the topics listed there are present

* Navigate to the `OTU browse page`- on the taxon name page for "xenasteiae" by finding the `OTU [ ]` section to the top right and clicking the `OTU navigator icon` (closed hexagon, right pointing arrow).

* Click the `radial navigator`
* Click the `Citations` slice
* Click the `blue pin icon`

 A reminder that this assigns the defaulted source on the pinboard as the source.

* Click `is original`
* Click `Create`

At this point you will see a list of topics come up. Those topics on your pinboard are shown first.

* Click `All`
* One at a time click `Biological control` then `create`, repeating for "Biology", "Diagnosis (Taxonomic)", "Distribution" and "Figured, adult"

For each, if you wish, it is possible to provide the page on which the topic is pertinent. Whether or not to do this will be up to the curation team.

* Click `X` to close the radial modal
* Reloading the `Browse taxa` should list the topics (again, crudely for now)

_Aside_: At this point you are thinking "didn't we do this, i.e. link a source to 'xenasteiae'"? Yes, but no. We know that we can track biological taxa separate from nomenclatural entities. Imagine a case of synonymy, where the biological taxon has already been described, and many bits of data have been attached to it. In that case we would want to attach our distribution, host, etc. information to the already defined/described taxon, not the record of the nomenclature in the citation. Imagine another case where an author has described a species whose type series includes two different *families* of insects (yes, it happens). Clearly we must decouple the names from the biological data in that case. These are some of the many reasons we keep names and taxa separate.

#### Distributions (asserted)

TaxonWorks captures distribution data in a couple of ways. Asserted Distributions are assertions that some taxon, according to some source, is present in some geographic area (at present this is limited down to level 3 subdivisions, e.g. counties type entities in the United States). Alternately collecting event data and georeferences on that data, which are linked to collection objects can be used.

For the purposes of a large curatorial project we'll assume that we want to capture the gross distribution, therefor we'll just detail how to use Asserted Distributions here.

* Find an `OTU radial` for `xenasteiae` (blue, hexagon of dashed lines). Remember they are found in a number of places, including the `OTU browse task` and the `Citations by source` page. The `Browse OTU` page is a good place to start. A reminder that the `OTU navigator` (blue, solid hexagon with arrow) takes you to the `OTU browse page`
* Click the `OTU radial`
* Click `Asserted distributions`
* Click the `blue pinned icon` to set the pinned source
* Search for "Karnataka". Note that two records are found. The underlying gazetteer in TaxonWorks draws from multiple sources, most of which have underlying geospatial representations. It is up to the curatorial team which gazetteer to favour. For now, choose the record from "TDWG Level 4.". The record is automatically created.
* Close the modal window

That's all there is too it.

##### Biological associations

The last major step is to add the biological associations asserted in the paper. In TaxonWorks we link OTUs together through biological relationships. See the "Addendum - Biological relationships" to ensure you have the necessary relationships created before continuing.

* Navigate to an `OTU radial` for `Ooencyrtus xenasteiae`. (This can be reached via the Browse taxa task, if you have forgotten how to find one.)
* Click the `OTU radial`
* Click 'Biological associations`
*	Under Biological relationship click the `Search button`
*	Search for "Parasitoid"
*	Select (click) the target record

Note that this, and other things like it are "Smart selectors", they learn from recent choices, your pinboard enteries, and other factors. Subsequent use will show the relationship you just used as a recent button.

* Under the `Related` section
* Ensure the `OTU` button is selected (button is white)
* Ensure the `Search` button is selected
* Type "Xenasteia sp." in the `Select an OTU`.
* When the search finishes you will see `--None--` and a `New` button pop up beside it
* Click `New` to create a new OTU on the fly
* In the `Taxon name` field that pops up search for and select `Xenasteia`
* Click `Create`

Note that the complete biological association is now spelled out above you. "Ooencyrtus xenasteiae" Parasitoid [of] Xenasteia sp.". If when using this form the relationship has an inverted name (see the `Biological relationship composer` task for more on building Biological Relationships) you can flip it to read from the perspective of the host.

* Click the now familiar `blue pin` to assign the pinned source
* Fill in "262" in `pages`
* Click the `"Is original" checkbox`

You are asserting this is the first time this relationship has been described. By definition it must be since the species was not known before this.

* Click create
* Close the modal window

Notice that we used "Parasitoid" when the paper says "Pupal parasitoid". It is up to the curators of the project to determine what level of granularity you wish to capture data at. You could in theory add more specific biological relationships.

##### Common names

Since the authors list a couple of common names let's go ahead and add them.

* In the `Browse nomenclature` task navigate to the name `Calophyllum inophyllum L.`

Notice that the `OTU navigator` button is green. No OTU has been created for this taxon yet.

* Click the `OTU navigator` button

You are taken to the `Browse taxa` task (homepage for an OTU).

* Click the `OTU radial` (hexagon, dashed lines)
* Click `Common names`
* Fill in "Indian laurel" in the `name field`
* Search for and select "India". The search will find several hits. Use the one from the ["Country"] dataset
* Search for and select "English" in `language`
* Leave the year fields blank.
* Click `Create`

* Repeat the steps for 'rugose spiralling whitefly' for "Aleurodicus rugioperculatus"

### Wrapping up

An alternate view to what has been added is available in the `Citations by source` task. You can get to this task from `Browse taxon names` by scrolling down to the references cited section and clicking on the `blue Navigate radial` icon besides the source in question then selecting the `Citations by source` slice. Anytime you see this icon you can navigate to the `Citations by source` task (and others). Alternately you can access the task through the `task tab`, then search for the target source.

## Addendum

### Manage biocuration classes and groups

_Aside_: You can also create, edit and update the individual groups and classes in the `Manage controlled vocabulary task`, but you can not combine the two there.

* Navigate to the `TASKS tab`, then find and click the `Manage biocuration classes and groups card`

Individual attributes are created on the right. Groups of attributes ("sex") and their membership are created on the left. You must provide a definition'. Be precise; what you do now will affect those interpreting your data years from now. Take some time to search Bioportal for other's concepts and re-use or cross-reference them if possible.

Add a new biocuration group.

* Put "Sex" in `name`
* Cross reference bioportal - `http://bioportal.bioontology.org/search?utf8=✓&query=sex`. Let's use the PATO (phenotype and traits ontology) definition (from http://bioportal.bioontology.org/ontologies/CLO?p=classes&conceptid=http%3A%2F%2Fpurl.obolibrary.org%2Fobo%2FPATO_0000047): "An organismal quality inhering in a bearer by virtue of the bearer's ability to undergo sexual reproduction in order to differentiate the individuals or types involved. Term applied to any organism able to undergo sexual reproduction in order to differentiate the individuals or types involved. Sexual reproduction is defined as the ability to exchange genetic material with the potential of recombinant progeny. The assemblage of physical properties or qualities by which male is distinguished from female; the physical difference between male and female; the distinguishing peculiarity of male or female.".
* Add the `URI` `http://purl.obolibrary.org/obo/PATO_0000047`

If you have no reservations with the definition use a `skos::ExactMatch` in URI relation. This is probably the least important field here, just referencing a URI adds the most information.

Add two biocuration sexes.

* On the right add "Male", and "Female". Add your own defintions or clone them from Bioportal- there are a lot of different concepts out there, even for "straightforward" concepts like sex, so don't take what you think you are expressing as forgranted.

Add the biocuration classes to the group.
* On the left, under "Sex", select and add both male and female to the group with the "Add to group" button.

A pragmatic note- groups are not as useful in the interface as the attributes themselves, i.e. you can get away with just creating biocuration classes without groups in most cases. Alternative you can add a single group and add all classes to it, this is useful in some task interfaces.

### Adding Topics

Topics are used in conjunction with a Citation, they form statements of the type "For the subject X, as seen in source Y, there is information on topic Z".

Topics in TaxonWorks are a user definable controlled vocabulary term. To create a topic:

* Navigate to the `TASKS tab`
* Click the `Manage controlled vocabulary` card
* Click the `Topic` button
* Make a quick search for the term to see if it is present
* If not present:
* Add a `Name` (term)
* Add a `Definition`

Definitions must be 20 characters. Don't neglect this or provide a "fake" definition to get past the requirement. Take some time to describe your meaning and intended use and interpretation. Others will be reading these definitions to figure out whether or not they are applicable to the contexts that they are in.

 If you wish, choose a color by clicking on the `CSS color swatch`. This will be used as a background to the name in some cases.

* Click the 'Create` button.

The Topic is inserted at the top of the list to the right.

You may wish to pin this topic to your pinboard with the `Green pin icon` to the right of the record.

For this exercise, add, or check to see that the following topics are present:

* "Diagnosis (Taxonomic)" - The paper contains a section which contains morphological characters which uniquely identify a taxon.
* "Biology" - The paper contains information on the biology of the organism.
* "Biological control" - The paper references this organsim in the context of biological control.
* "Distribution" - The paper contains information on the distribution of this organism.
* "Figured, adult" - The paper contains figures an adult of a organism.
* "Hosts" - THe paper contains information on the hosts of this organism.

_Aside_: It is worth checking BioPortal or other sources for definitions that might match your topic. EOL has sets of topics, etc. If you can find a URI (a unique identifier for a topic/concept) include it in the record.

### Adding biological relationships

* Navigate to the `TASKS tab`
* Use the `B Biology` link on the filter to filter the cards
* Click on `Biological relationship composer` task

* Under `Edit`, in `Name` type `Parasitoid`
* Click `Create`

There are two perspectives in a relationship, from the left, and from the right. If we have A host B then we read "A host *of* B". In the interface we can invert this if we provide term for for the inverse relationship.

* Click `Flip`
* Add "Host" to `Inverted name`
* Click `Update`

The relationship is not transitive, so we don't click that check. That is, we can *not* infer the following is true:
```
A parasitoid B
B parasitoid C
A parasitoid C
```

It is also not reflexive (wasps are parasitoids of hosts, but hosts are not parasitoids of wasps).

For this exercise ensure the following relationships are added:

* Plant associate
* Associate
* Parasitoid / Host
* Plant host
* Primary host

_Aside:_ If you see a term already present in the list on the left you can click on it to edit it and see example use if it has been used already.  You can also extended the meaning of your relationship through the use of `Properties`, to be described elsewhere.
