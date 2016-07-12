# Instamojo_CI
Instamojo Payment API Library for CodeIniter

Assists you to programmatically create, edit and delete Links on Instamojo in CodeIngiter PHP Framework.

**Note**: If you're using this wrapper with Instamojo's sandbox environment `https://test.instamojo.com/` then you should change the endpoint in the Instamojo library to the sandbox environment.

    $endpoint = 'https://test.instamojo.com/api/1.1/';
    
## Usage

### Create a new Payment Request
    $this->load->library('instamojo');
    try {
        $response = $api->paymentRequestCreate(array(
            "purpose" => "FIFA 16",
            "amount" => "3499",
            "send_email" => true,
            "email" => "foo@example.com",
            "redirect_url" => "http://www.example.com/handle_redirect.php"
            ));
        print_r($response);
    }
    catch (Exception $e) {
        print('Error: ' . $e->getMessage());
    }

This will give you JSON object containing details of the Payment Request that was just created.

You can refer to [Instamojo Native PHP Library](https://github.com/Instamojo/instamojo-php) for more functions.
