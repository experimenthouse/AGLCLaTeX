# AGLCLaTeX
Biblatex style for the Australian Guide to Legal Citation

## Background

I made a nearly-complete Biblatex style some years ago, but was never fully happy with it. This is an attempt to start again from the ground up.

The Australian Guide to Legal Citation is a law-focused citation style that relies on footnotes, and usually does not include a bibliography (but can). It is one of the more flexible and easy-to-use citation styles, with clear and simple rules.

## Observations

Rather than use footnotes automatically, it may be better to provide a separate citation command that can be wrapped within a footnote, such as `\footnote{\cite{ab2000}}` to allow in-text citations. This may have implications for citing sources above and below because the footnote number will have to be captured.

## General rules

Some of the general rules are up to the author to implement, such as footnote positioning, but others can be implemented by the Biblatex style.

| Rule                  | Implementation                                                       |
|-----------------------|----------------------------------------------------------------------|
| Multiple sources      | Separate sources with a semicolon (';') unless separate introduction |
| Full stops            | Automatically add a full stop at the end of the citation             |
| Pinpoint references   | Special command for paragraph pinpoints                              |
| Introductory signals  | Special commands for introductory signals                            |
| Quotes/citations      | Special commands for sources referring to other sources              |
| Immediate references  | Print 'Ibid' (with pinpoint)                                         |
| Subsequent references | Print short name with 'above n' (with note number)                   |
| Short titles          | Print source followed by short title, then use short title in future |
| Long quotations       | Define quotation environment to indent and use smaller font          |
| DD Month YYYY dates   | Use Babel Australian parameter                                       |
| Multiple authors      | Separate with commas and 'and', with 'et al' for more than three     |
| Titles and headings   | Provide a custom document class                                      |
| Bibliographies        | Utilise some form of taxonomy                                        |
