# ShinyRemdat
## About

Disasters wordwide from 1900-2008 A comprehensive listing of of over 17,000 disasters, natural and otherwise, from around the globe.

## At a minimum, running this application requires the packages named **shiny**, **ggplot2** and **Remdata**, install them, in R, like this:


`install.packages("ggplot2")`

`install.packages("shiny")`

`install.packages("devtools")`

`library(devtools)`

`install_github("botanyhelp/Remdata")`


Installing the shiny R package on an Apple Mac generally requires that the Mac have Xcode installed.  

## Starting ShinyRemdat on the Internet or local network

ShinyRemdat is a single file application located in app.R.  It can be started with R from the command line like this, if the ShinyRemdat folder is in your home directory:

`sudo nohup R -e shiny::runApp('~/ShinyRemdat/app.R',port=8787,host=getOption('li1077-179.members.linode.com')) &`

..and then the application will be visible on the server on the host where it was started, in this example case, here:

[ShinyRemdat](li1077-179.members.linode.com:8787)

..technically you won't need either the **sudo** nor the **nohup** parts of the command because any user can start a server listening on port 8787, as we do in the example.  To listen on port 80, for example, you would require **sudo** or you would need to start it as root.  Port 80 would need to be free on that machine:

`sudo nohup R -e shiny::runApp('~/ShinyRemdat/app.R',port=80,host=getOption('li1077-179.members.linode.com')) &`

## Starting ShinyRemdat locally

Starting from a linux shell works like this:

`R -e shiny::runApp('~/shinyRemdat/app.R')`

Starting from the Terminal App on a Mac works like this:

`R -e 'shiny::runApp("~/ShinyRemdat/app.R")'`

..and causes output like this to appear.  Here we can see that the Mac selected port 7005 to run the shiny server.  In this case the URL where the application was running would be **http://127.0.0.1:7005** which can be opened by a web browser running on the same machine.  


`R version 3.2.1 (2015-06-18) -- "World-Famous Astronaut"`
`Copyright (C) 2015 The R Foundation for Statistical Computing`
`Platform: x86_64-apple-darwin10.8.0 (64-bit)`
``
`R is free software and comes with ABSOLUTELY NO WARRANTY.`
`You are welcome to redistribute it under certain conditions.`
`Type 'license()' or 'licence()' for distribution details.`
``
`  Natural language support but running in an English locale`
``
`R is a collaborative project with many contributors.`
`Type 'contributors()' for more information and`
`'citation()' on how to cite R or R packages in publications.`
``
`Type 'demo()' for some demos, 'help()' for on-line help, or`
`'help.start()' for an HTML browser interface to help.`
`Type 'q()' to quit R.`
``
`> shiny::runApp("~/ShinyRemdat/app.R")`
`Loading required package: shiny`
``
`Listening on http://127.0.0.1:7005`


## Licensing 
See LICENSE file, hint: GPLv3

The data in the Remdata package used by this shiny app **ShinyRemdat** is generously shared by the EMDAT people at www.emdat.be.  Here is what they say about it:

Disasters wordwide from 1900-2008 A comprehensive listing of of over 17,000 disasters, natural and otherwise, from around the globe.

Since 1988 the WHO Collaborating Centre for Research on the Epidemiology of Disasters (CRED) has been maintaining an Emergency Events Database EM-DAT. EM-DAT was created with the initial support of the WHO and the Belgian Government.

The main objective of the database is to serve the purposes of humanitarian action at national and international levels. It is an initiative aimed to rationalise decision making for disaster preparedness, as well as providing an objective base for vulnerability assessment and priority setting. For example, it allows on to decide whether floods in a given country are more significant in terms of its human impact than earthquakes or whether a country is more vulnerable than another for computing resources is.

EM-DAT contains essential core data on the occurrence and effects of over 16,000 mass disasters in the world from 1900 to present. The database is compiled from various sources, including UN agencies, non-governmental organisations, insurance companies, research institutes and press agencies.

This is only public domain natural disaster database around (two other global sources are private: Sigma from Swiss Re and NatCat from Munich Re).

The EM-DAT database is protected by the law of 30 June 1994 on copyright and the law of 31 August 1998 on the legal protection of databases.

EM-DAT was created in 1988 at the Université Catholique de Louvain by researchers at the Centre de Recherche sur l’Epidemiologie des Desastres – Centre for Research on the Epidemiology of Disasters (CRED). The database was set up with the support of the WHO and the Belgian government. Since 1999, CRED has received support from the Office of Foreign Disaster Assistance (OFDA) of the US Agency for International Development (USAID). The Université Catholique de Louvain holds the copyright for the database.

The EM-DAT database has been made available for unrestricted access free of charge by UCL so that anyone with a query can obtain information.

EM-DAT: The OFDA/CRED International Disaster Database – www.emdat.be – Université Catholique de Louvain – Brussels – Belgium.
