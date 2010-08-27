## Usage

    require_once '/path/to/swift-mailer/lib/swift_required.php';
    require_once '/path/to/postmark_swiftmailer.php';
    
    $transport = Swift_PostmarkTransport::newInstance('YOUR-POSTMARK-API-KEY')
    $mailer = Swift_Mailer::newInstance($transport);
    $message = Swift_Message::newInstance('Wonderful Subject')
      ->setFrom(array('sender@mydomain.com' => 'John Doe'))
      ->setTo(array('receiver@otherdomain.org' => 'Jane Doe'))
      ->setBody('Here is the message itself');
    $mailer->send($message);
