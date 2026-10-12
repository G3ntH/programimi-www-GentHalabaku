Java III: Klinika e CSS, shpëto afishen
Afishja e klubit të debatit, e kthyer në një ftesë të qartë me CSS të jashtëm.

Skedarët
index.html: struktura e afishes (titull, datë, vend, përshkrim, lidhje regjistrimi).
style.css: variablat (:root), baza, etiketat, butoni dhe gjendja :focus-visible.
gabime.css: diagnoza dhe rregullimi i konfliktit dhe i tejkalimit të gjerësisë.
Etiketat
Tri etiketa që nuk dallohen vetëm me ngjyrë: tekst i ndryshëm dhe stil i ndryshëm i kornizës (vijë e plotë, e ndërprerë, e dyfishtë).

Box model dhe box-sizing
Gjerësia totale e një kutie = width + padding + border (majtas e djathtas).

content-box: width vlen vetëm për përmbajtjen. 200 + 2×20 + 2×5 = 250px.
border-box: width përfshin padding dhe border. Kutia mbetet 200px. Demonstrimi është në fund të faqes. Në style.css përdoret border-box për të gjithë elementet.
Gjendja e fokusit
a:focus-visible ka kontur 3px me largësi 3px. Shihet kur lëviz me Tab (skip link, pastaj butoni i regjistrimit).

Rastet e pranimit
done
CSS ngarkohet nga skedar i veçantë.
done
Paneli nuk del nga ekrani 360 px (width: 100% me max-width, padding me clamp).
done
Teksti lexohet mbi sfond dhe fokusi shihet me Tab.
Reflektim: cili rregull fitoi në kaskadë dhe pse?
Rregulli #poster (color: white). Selektori me id ka specifikë më të madhe (1,0,0) se ai me klasë .poster (0,1,0), kështu që fiton pa marrë parasysh rendin. Rezultati ishte tekst i bardhë mbi sfond të bardhë. E rregullova pa !important: hoqa stilimin nga id-ja dhe i vendosa të gjitha rregullat në klasën .poster.