python-oembed
=============

Python library that implements an OEmbed consumer to use with OEmbed providers. This is a fork of the 
`Google Code project <http://code.google.com/p/python-oembed/>`_. For more reference, please refere to the original project's webpage. 

The main additions in this fork are:

* Updated OEmbed provider rules.
* Rudimentary but working auto-discovery of endpoint URL's


Usage::

    import oembed

    consumer = oembed.OEmbedConsumer()
    endpoint = oembed.OEmbedEndpoint('http://www.flickr.com/services/oembed', \
                                     ['http://*.flickr.com/*'])
    consumer.addEndpoint(endpoint)

    response = consumer.embed('http://www.flickr.com/photos/wizardbt/2584979382/')

    print response['url']

    import pprint
    pprint.pprint(response.getData())
