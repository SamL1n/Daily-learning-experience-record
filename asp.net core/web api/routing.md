### Routing in Web Api

``` C#
    [Route("api/[controller]")]  //equals to [Route("api/book")]
    [ApiController]
    public class BookController : ControllerBase
    {
        [HttpGet] //api/book
        public IActionResult GetBooks()
        {
            return NoContent();
        }

        [HttpDelete("{id}")] //api/book/1
        public IActionResult DeleteBook(int id)
        {
            return NoContent();
        }

        [HttpDelete("all")] //api/book/all
        public IActionResult DeleteAllBooks()
        {
            return NoContent();
        }
    }
```