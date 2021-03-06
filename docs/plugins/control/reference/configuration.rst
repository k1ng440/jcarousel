Configuration
=============

The plugin accepts the following options:

.. _control.reference.configuration.target:

``target``
    The target for the control. Accepts the same argument as the
    :ref:`scroll() <reference.api.scroll>` method.

    **Example:**

    .. code-block:: javascript

        $('.jcarousel').jcarouselControl({
            'target': '+=3'
        });

    **Default:**
        ``+=1``

.. _control.reference.configuration.event:

``event``
    The event which triggers the control.

    **Example:**

    .. code-block:: javascript

        $('.jcarousel').jcarouselControl({
            'event': 'mouseover'
        });

    **Default:**
        ``click``

.. _control.reference.configuration.method:

``method``
    The method to call on the carousel.

    Plugins may provide alternate methods for scrolling the carousel, e.g.
    ``scrollIntoView`` from the :doc:`../../scrollintoview/index`.

    Alternatively, ``method`` can be a function which will be called in the
    context of the plugin instance.

    **Example:**

    .. code-block:: javascript

        $('.jcarousel').jcarouselControl({
            'method': 'scrollIntoView'
        });

        $('.jcarousel').jcarouselControl({
            'method': function() {
                this.carousel()
                    .jcarousel('myScrollingMethod', this.options('target'));
            }
        });

    **Default:**
        ``scroll``
