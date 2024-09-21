# EUDAMED API Reference (unofficial)

Unofficial API reference for EUDAMED, the European database of medical devices.

[View the API reference here.][html]

More links:

* [BEUDAMED: Better EUDAMED search engine][beudamed]. Use this to explore EUDAMED data in a fast, modern and
  user-friendly way.
* [EUDAMED][eudamed]: The original search engine, whose API this repository refers to. Use this to explore
  EUDAMED data in the, umm, *original* way.

## Rationale

The introduction of a unified database for medical devices across all European countries is a good idea - it
creates transparency, collects all data in one place and reduces overhead as each country no longer has to
maintain their own infrastructure.

Well, that's the theory.

Unfortunately, EUDAMED has, politely speaking, not really delivered upon those promises. Its user experience
is somewhere between "huh, this feels like Windows 95" and "I'm throwing my computer out of the window
now". Running a search easily takes 5 - 10 seconds. You can't right-click on links (?), so good luck managing
your research in multiple tabs (you can't).

It's the best example of what happens when you develop "software by committee".

And it's not even feature-complete. Its timeline for completion has been postponed multiple times. It's still
being developed as we speak.

This is saddening to see, because it hampers innovation and makes people unhappy: Every minute in the EU,
there's probably a person wrestling with EUDAMED and throwing their hands up into the air (or their computer
out of the window).

Not every regulator is bad at writing software: In the US, the FDA has launched a project called
[openFDA][openfda] which provides both a simple API to access data, and machine-readable data dumps of all
data for offline processing. It's very cool.

Now, what to do in the EU?

The EU is not really delivering (at least before 2027, see below), but we can do some things about this.

We aim to achieve two things:

1. Build a better Eudamed search engine so that EU medical device innovation is no longer hampered by terrible
   software.
2. Create transparency about APIs, so that others can hook into the data and contribute.

Goal #1 is solved by [BEUDAMED][beudamed], or "[Better EUDAMED][beudamed]", which we developed. It provides a
much better user experience for searching across the EUDAMED data (think of it like Google Scholar
vs. Pubmed).

Goal #2 is solved by this repository. While building BEUDAMED, we learned a lot about the EUDAMED API and data
structure (spoiler: it's a mess), so we've summarized all our learnings here and hope that other people will
contribute.

Maybe that will enable other developers to build useful software on top of EUDAMED in the future.

You still have ample time: EUDAMED is only planned to be complete by 2027. The timeline was moved most
recently in July 2024.

## Contributing

You can view the API definition (which is a yml file) [here][yml]. The most straightforward way to edit it is
to copy-paste its content into the [Swagger Editor][swagger-editor] (or the newer [Swagger Editor
Next][swagger-editor-next], no clue which one is better).

Based on the yml file, this GitHub repository builds a HTML file with [redocly-cli][redocly-cli] and pushes it
to the [GitHub pages site][html].

Open a pull request if you'd like to propose changes.

## OpenRegulatory

Hold on, who the hell are we?

We're [OpenRegulatory][openregulatory], and it's our mission to enable for medical device innovation by making
it much easier, affordable and transparent to comply with medical device regulations.

For that purpose, we've published all our [MDR / ISO 13485 templates for free][templates] (also on
[GitHub][templates-github]). And we've built a [QMS Software][formwork] which enables lean, founder-led
Healthcare startups (like yours?) to enter the market faster, because a lot of the regulatory documentation
gets automated by it.

That's it. Have a nice day!

.. and I hope browsing the EUDAMED API documentation is less painful for you than it was for me when I was
writing it. Because it's truly a mess.


<!-- Links -->

[html]: https://openregulatory.github.io/eudamed-api/
[eudamed]: https://ec.europa.eu/tools/eudamed/eudamed
[beudamed]: https://beudamed.com
[openfda]: https://open.fda.gov
[yml]: eudamed_api_openapi_3_1.yml
[swagger-editor]: https://editor.swagger.io
[swagger-editor-next]: https://editor-next.swagger.io
[redocly-cli]: https://redocly.com/docs/cli
[openregulatory]: https://openregulatory.com
[templates]: https://openregulatory.com/templates
[templates-github]: https://github.com/openregulatory/templates
[formwork]: https://openregulatory.com/formwork
