import requests
from bs4 import BeautifulSoup

# all urls that need to be scraped
urls = ["https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/ProductsPurchase", 
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/DigitalProducts",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/ReturnGoods",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/ManufacturerWarranty",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/OrderCancellation",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/Pricing",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/PaymentMethods",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/OrderDeliveryShipping",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/Newsletters",
        "https://www.plaisio.gr/Help/MyServices/MyOrder/OrderDelay",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/DisputeResolution",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/Article39",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/Clearance-items",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/Stockhouse-items",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/GiftcardsCoupons",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/Recycle",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/EuropeanReliance",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/Services",
        "https://www.plaisio.gr/Help/SupportAndGuidance/PlaisioSupport/PlaisioTermsOfWarranty",
        "https://www.plaisio.gr/Help/GeneralInformation/LegalFramework/TermsOfUse/ProductReviews"]

# method that scrapes each url
def scrape(url):
    content = requests.get(url).text
    soup = BeautifulSoup(content,'html.parser')

    # get the page title
    title = soup.find("title")
    # get the text that you want
    all_text = soup.find("div", class_="help-page__content").find_all("p");

    print ("\n")
    print ("\n")
    print (title.text)
    print ("\n")
    for p in all_text:
        print(p.text)

# scraping time
for link in urls:
    scrape(link)
