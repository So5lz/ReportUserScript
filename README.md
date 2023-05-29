# ReportUserScript
UserReportScript
this script is for a game that mass-reports a user.

copy here-/
import requests

def report_user(url, user_id, reason):

    """

    Reports a user online by sending a POST request to the specified URL with the given user ID and reason.

    """

    data = {

        "user_id": user_id,

        "reason": reason

    }

    response = requests.post(url, data=data)

    if response.status_code == 200:

        print("User reported successfully.")

    else:

        print("Failed to report user. Status code: {}".format(response.status_code))

# Example usage

url = "https://example.com/report"

user_id = "12345"

reason = "This user is spamming the chat room."

report_user(url, user_id, reason
