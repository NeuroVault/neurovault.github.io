---
layout: post
title: "A Decade of Openly Sharing Brain Maps!"
categories: updates
date: 2023-05-20
---

by Alejandro de la Vega

*Special thanks to Julio Peraza, Kendra Oudyk and Ross Blair for data retrieval and analysis for this post.*

**TLDR: We need your help! We want to learn about why people use NeuroVault and how we can improve it to incentivize uploading, data re-use and keep up with changes in the field. [Please take a few minutes to tell what it should look like](https://tally.so/forms/wLP2Oj)!**

---

It's hard to believe, but it's been over 10 years since NeuroVault was first launched. 

In 2013, at the [Neurosynth Hackathon](https://web.archive.org/web/20131202224713/http://hackathon.neurosynth.org/) in Boulder, Colorado, Chris Gorgolewski furiously typed away at his laptop, and three days later with the help of lots of coffee and Tal Yarkoni's ever watchful gaze, NeuroVault was born! 

The mission was simple: to provide a place where researchers can publicly store and share unthresholded statistical maps, parcellations, and atlases produced by MRI and PET studies. 

*The reason?* Neuroimaging studies are expensive, but they're often underpowered, and statistical results are summarized into static figures and thresholded peak coordinates buried in articles, discarding a wide range of valuable information. Although the field of neuroimaging has significantly advanced since 2013--with notably larger *and* deeper samples becoming more common-- the core mission of NeuroVault to enable public sharing of neuroimaging results remains equally relevant.

As an attendee of that hackathon in Boulder (in fact, it was my very first one!), I'm happy to say that nearly 11 years later, **NeuroVault is very much alive and well**. NeuroVault is visited by *nearly 30,000 users a year*, and boasts a *staggering 269,934 images* contributed by 3,216 unique users!

I want to take some time to dive into this wealth of data to understand it, and ask *in what ways NeuroVault has succeeded, and how we can continue to improve the platform to make sure the next decade of data sharing is even better than the last*.

Now let's dive into some numbers!

### What has been uploaded to NeuroVault?

The first image was uploaded to NeuroVault on June 6th, 2013, featuring the statistical maps of "Escaping the here and now: Evidence for a role of the default mode network in perceptually decoupled thought" by Smallwood et al.

Since then, the number of collections uploaded to NeuroVault has steadily increased, reaching a peak in 2023 with 778 collections uploaded. Although only around 15% of collections of are associated with the DOI of a published article, this figure is dragged down by the most recent years (scientific articles are slow to be published) and incomplete meta-data which I'll come back to this later.

![images_by_year](./_images/01_collections_by_year.png)

The number of images uploaded per year varies much more, reaching a peak in 2021 with 60,441 images. A majority of images are annotated using the Cognitive Atlas Ontology, for both Task and Contrast IDs (see the Cognitive Atlas website for more information), providing critical meta-data for subsequent re-use.

(Images Plot)

Unsurprisingly, the vast majority of images of NeuroVault are "fMRI-BOLD", with other modalities comprising a small minority. Perhaps future iterations of NeuroVault should increase outreach to other neuroimaging communities. 

(Modality plot)

(what are the other modalities?)

In keeping with the spirit of NeuroVault, around 3/4 uploaded images are unthresholded, meaning the full richness of the data is maintained. Similarly, over 3/4 of images in NeuroVault are statistical maps (Z or T), with other types of images (such as variance and effect maps), making up a smaller proportion.

Somewhat surprisingly, 88% of images in NeuroVault are from individual subjects, with only 10% of images corresponding to group-level maps. 

(single vs group map)

However, this is mostly driven by a few rather large collections. Looking only at 2,240 collections associated with a DOI and sufficient met-data, 190 collections have single subject data while have 1844 group-level data.

(pie chart, type of images) 

Speaking of large collections, the award for largest collection on NeuroVault associated with a published article goes to ["Brain topography beyond parcellations: Local gradients of functional maps"](https://neurovault.org/collections/16103/) by Dohmatob et al. (2021). This collection features a staggering 29,464 images. Impresive!

### Increasing NeuroVault adoption

At this point, you might be under the impression that NeuroVault is unequivocally a success. Although, the longevity of the platform is certainly impressive, there is much progress to be made. 

Using full text neuroimaging articles on PubMedCentral as a representative sample, we find that although the proportion of studies using NeuroVault to share their data has increased year to year, a large proportion of studies continue to only report peak coordinates in a table, limiting the potential re-use of their valuable data in the future!

(time plot)

Please remember to continue to share NeuroVault with your colleages, and share ideas you might have for increasing NeuroVault adoption in our survey!

### Linking NeuroVault data to scientific knowledge

To truly understand what is uploaded NeuroVault, it helps to link published articles to the collections that contain the relevant data. However, a surprisingly small proportion of collections are ultimately linked to publications. 

This is part due to the fact that most users upload data to NeuroVault prior to submitting their articles, and must remember to go back and tag their collection with the final DOI. Indeed, the average time between when a collection is created and ultimately linked with a DOI is 154 days, with some collections taking over 4 years to get a DOI! Unfortunately, this sometimes never happens. 

(time histogram)

Using a couple tricks, however, we can infer the most likely article to be associated with  collections. By searching PubMed for NeuroVault titles, and searching full text literature for NeuroVault links, we're able to link several hundred more collections, increasing the number of collections with a DOI to XXX (~25%)! 

This is likely an underestimate, since we don't have access to the entirety of the neuroimaging literature to find all possible NeuroVault links. In the future, it may be helpful to automatically remind users to link their collections with published articles after some time has passed.

### Is NeuroVault data representative of the literature?

Now that we have linked as many collections to DOIs as possible, we can ask: what type of studies are uploaded to NeuroVault?

(word cloud)

Just from looking at the most commonly used words in articles in NeuroVault, we can that a wide variety of topics are covered, with working memory being the most commonly studies subject.

But, is this representative of the literature at large? To answer this question, we can compare the distribution of topics derive using a larger sample of fMRI literature (XXX studies, obtained using Pubget), and comparing the number of studies that load onto each topic from a larger sample and the NeuroVault sample.

(Kendra plot)

Unsurprisingly, working memory is the most studied topic in both samples. Generally, it also seems that many well-studies topics are represented in NeuroVault.

However, many commonly studies topics seem to be under-represented relatively to the literature. In particular, topics related to "depression", "epilespy", "recovery", "ms" and many other clinically relevant terms are under-represented in NeuroVault relative to the broader fMRI literature. This potentially indicates we can do a better job as basic science researchers in reaching out to clinical researchers, to ensure they contribute their valuable data to open access repositories, such as NeuroVault.

### Is NeuroVault data *re-used*?

The main goal of the NeuroVault project was not simply to gather as many statistical maps as possible for fun. The critical point of this project is to facilitate access to this valuable data to enable new downstream meta-scientific use cases, such as large-scale image-based meta-analysis and ROI creation.

To estimate data re-use, we again looked at a representative sample of published neuroimaging studies, and tried to find collections which were mentioned at least *twice* in the literature. Presumably, collections and images with multiple mentions were used in subsequent studies in some capacity. 

By this measure, ~23% of collections with a DOI were mentioned more than once, indicating that a respectable number of uploads are indeed re-used.

If we look at the most re-used images, we find that these are often atlases, rather than statistical maps. Congratuations to XXXX for being the most re-used collection on NeuroVault!

However, it's also clear that there is much more potential for re-use than we are currently achieving. For example, NeuroVault has built in capacity for image-based meta-analysis which has been used seldom, presumably because identifying relevant images for a manual meta-analysis is extremely challenging. 

If you're interested in performing an image-based meta-analysis, let me make a shameless plug for NeuroSynth Compose, the latest iteration of our open platform for large-scale meta-analysis. We are actively working on a web-based interface for image-based meta-analysis using NeuroVault data, which we hope to release in the coming months!

Also, don't hesitate to reach out to the NeuroVault if you need help accessing the data. We are happy to help!

## You turn: help guide the future of NeuroVault

Overall, for a relatively simple application, NeuroVault has gained remarkable traction in the neuroimaging field. 

But, as I hope you appreciate now, there is much work to be done to increase NeuroVault adoption and the re-use of this valuable data.

Be share to share your thoughts with us using our survey, and be sure to reach out directly to us with any constructive ideas. 

Let's make sure the next decade of open neuroimaging data sharing is even more successful than the last.


