# discipl-core-tlswitness

connector that enables a discipl node to be used as a trusted TLS Witness proxy and use it through the Discipl Core API

client device with for instance IRMA wallet connected to discipl node as TLS witness proxy using organisation key registry of NLX node hosted by municipality (Pijnacker):
discipl.claim('did:discipl:irma','link:discipl:tlxwitness-http://mijnoverheid.nl/brp/overzicht#Woonplaats#PG1ldGEgbmFtZT0iaG9zdG5hbWUiIGNvbnRlbnQ9ImdpdGh1Yi5jb20iPig/OlxzKik8bWV0YSBuYW1lPSJ1c2VyLWxvZ2luIiBjb250ZW50PSIoXFMrKSI+', 'Pijnacker')

verifier device using IRMA attribute verification (works even without internet temporarily):
let link = discipl.claim('did:discipl:irma','tlxwitness-http://mijnoverheid.nl/brp/overzicht#Woonplaats#PG1ldGEgbmFtZT0iaG9zdG5hbWUiIGNvbnRlbnQ9ImdpdGh1Yi5jb20iPig/OlxzKik8bWV0YSBuYW1lPSJ1c2VyLWxvZ2luIiBjb250ZW50PSIoXFMrKSI+', 'Pijnacker')
discipl.verify(link, 'did:discipl:nlx-mijnoverheid')

where the given predicate in the claim is registered as IRMA attribute by the mijnoverheid NLX did 

Note WIP, will probably change considerably
