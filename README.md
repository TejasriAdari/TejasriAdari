def send_sms(api_key, phone_number, message):
    url = f"https://textbelt.com/text?phone={phone_number}&message={message}&key={api_key}"
    response = requests.get(url)
    if response.status_code == 200:
        print("SMS sent successfully!")
    else:
        print("Failed to send SMS.")
    return response.status_code
