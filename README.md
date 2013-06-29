# Langtools
A simple language tool for PHP

# Usage

 1 Place langtools in a vendor folder of your app or similar.
 
 2 Create a file for each language definition in <PROJECT_ROOT>/lang/<LANGUAGE_CODE>.lang eg.

 /lang/se.lang


and the language file is a json filezconsisting of the language definitions:

    {
    	"count-plays": "Antal spelningar",
        "count-brought-plays": "Antal beställda spelningar",
        "progress": "Progress",
        "campaign": "Kampanj"
    }

In your header define a condition for which language to use, and then set the language to be used:

    $GLOBALS['lang'] = (strrpos($data['section'], 'eng') !== FALSE ) ? 'en' : 'se';
    require_once 'vendors/langtools/langtools.php';

It's very important the require comes AFTER the language set.