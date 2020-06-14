# Webpage for Bath Numerical Analysis 

## Seminars
To set-up seminars on this web page, there are two files to take care of:
- in collections/ _posts/, create a template in a filename of the form year-month-day-seminar.md (using  approximate start dates for the semester's seminars). To create a new semester, copy from one of the 2020 posts. Edit the entries. In datafile=site.data.XXX, XXX is the name of  the following file.
- in _data/, create a template in a filename of the form XXX.yml. where XXX=seminars_academicyear_S{1,2}. The exact filename is referenced in the entry in the _posts/ directory (as mentioned above).

## Format of the data entries in the yml file

Individual seminars are listed. The format is
       
       - date: 1 Jan 2000 (the date and only the date in machine-readable format)
         speaker: name (uni)
         url: speaker_url (optional)
         title: my title (optional) 
         abstract: 'my abstract' (optional) (Use single quotes)
         inred: extra information that displays in red' (optional)
         cancelled: set true for cancelled seminar (optional)
         teams: url for online Teams seminar

Alignment of the keys (date, speakers, etc) is important. The entries are sorted on the date, which must be machine readable. Single quotes are important (if paragraphs are used). Mathematics is allowed (MathJax; e.g.,  $\alpha$ by using dollar signs).
An example entry is

      - date: 15 May 2020
        speaker: Jeremy Budd (Delft, Netherlands)
        title: Allen-Cahn and MBO on graphs 
        abstract: 'An emerging technique in clustering, segmentation and classification problems is to consider the dynamics of flows defined on finite graphs. In particular Bertozzi and co-authors considered dynamics related to Allen-Cahn flow (Bertozzi, Flenner, 2012) and the MBO algorithm (Merkurjev, Kostic, Bertozzi, 2013) for this purpose. This talk will exhibit our recent work showing rigorous links between these two flows, explaining why MBO can be used as an alternative to Allen-Cahn.'
        teams: 'https://teams.microsoft.com/l/meetup-join/19%3ad8aa162230c14a67a10243ac2f75d98d%40thread.tacv2/1588783928311?context=%7b%22Tid%22%3a%22377e3d22-4ea1-422d-b0ad-8fcc89406b9e%22%2c%22Oid%22%3a%22ca31603c-bea1-49a9-9542-de84a57ad77c%22%7d'

