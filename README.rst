================================================
LogPlus
================================================


Log Better

* Free software: MIT license
* Documentation: TBD


================================================
Installation
================================================

To install LogPlus::

    pip install logplus

    or

    pip install git+https://github.com/tactlabs/logplus.git

Pip installing the library from local repository::

    conda activate <env_name>

    python setup.py install develop

================================================
Usage
================================================

To use LogPlus in a project::

    import logplus

================================================
Sample
================================================

Example
::

    import logplus

    logger = logplus.get_logger()

    result_json = {
        'result': 1,
        'a' : "two",
        'b' : {
            "one" : "two"
        }
    }

    logger.info('message test')
    logger.info(result_json)
    logger.debug('message debug')
    logger.warning('message warning')
    logger.error('message error')

================================================
Output
================================================

    2024-05-12 16:29:28 info  [~/projects/logger-base/test.py:28][startpy] message test

    2024-05-12 16:29:28 info  [~/projects/logger-base/test.py:29][startpy] {'result': 1, 'a': 'two', 'b': {'one': 'two'}}

    2024-05-12 16:29:28 debug  [~/projects/logger-base/test.py:31][startpy] message debug

    2024-05-12 16:29:28 warning  [~/projects/logger-base/test.py:32][startpy] message warning

    2024-05-12 16:29:28 error  [~/projects/logger-base/test.py:33][startpy] message error

Credits
::

    The base code is derived from StructLog (https://github.com/hynek/structlog).
    As we see a lot of improvement in StructLog we came up with this library.