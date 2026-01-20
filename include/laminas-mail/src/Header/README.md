Headers
=======
Header field implementations and helpers for laminas-mail.

Contents
--------
- Core headers: From.php, To.php, Cc.php, Bcc.php, ReplyTo.php, Sender.php, Subject.php, Date.php, MessageId.php, References.php, InReplyTo.php, MimeVersion.php, Received.php, ContentType.php, ContentDisposition.php, ContentTransferEncoding.php.
- Infrastructure: HeaderInterface.php, MultipleHeadersInterface.php, GenericHeader.php, GenericMultiHeader.php, StructuredInterface.php, UnstructuredInterface.php, HeaderName.php, HeaderValue.php, HeaderWrap.php.
- Loading/parsing: HeaderLoader.php, HeaderLocator.php, HeaderLocatorInterface.php, ListParser.php, IdentificationField.php.
- Abstracts and helpers: AbstractAddressList.php.
- Exception/ – header-specific exceptions (BadMethodCallException, InvalidArgumentException, RuntimeException, ExceptionInterface).

Notes
-----
- Vendor code; avoid local modification. Refer to upstream docs at https://docs.laminas.dev/laminas-mail/.
- Header parsers must remain RFC-compliant; changes can break email interoperability.
