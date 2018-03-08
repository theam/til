Johan Sebastian Cortes M.

# Avoid CloudFront cache to check UI changes
Sometimes we need to check UI changes made to web pages cached with CloudFront, but we can't see it if that resource is already cached. In order to avoid the Time To Live of the cached resource, we can use a VPN service like Hola.org to load the page from a different region and by doing that we avoid the hit from CloudFront and we can check the change immediately.
