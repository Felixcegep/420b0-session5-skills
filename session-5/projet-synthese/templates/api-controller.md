# Gabarit contrôleur API ASP.NET

```csharp
[Route("api/[controller]")]
[ApiController]
public class RessourceController(IRessourceRepository repo) : ControllerBase
{
    [HttpGet]
    public async Task<ActionResult<List<RessourceResponseDto>>> GetAll()
    {
        return Ok(await repo.GetAllAsync());
    }
}
```
